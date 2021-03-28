---
title: "Extract Target Power Generation Facilities from AESO"
classes: wide
excerpt: "Petrinex Data"
categories: 
  - Data Science
tags:
  - Petrinex
  - Data Science
  - Oil and Gas
---


Alberta Electric System Operator (AESO) publishes electricity generation data in Alberta <http://ets.aeso.ca>

Download all monthly data files into Folder "Data". 

```python
import pandas as pd
import numpy as np
import glob
files = glob.glob('./data/*.csv')

```
Assigned column names

```python
col_names = ['PoolID','AssetType','AssetID',
             'Hour1','Hour2','Hour3','Hour4','Hour5','Hour6','Hour7','Hour8','Hour9','Hour10',
            'Hour11','Hour12','Hour13','Hour14','Hour15','Hour16','Hour17','Hour18','Hour19','Hour20',
             'Hour21','Hour22','Hour23','Hour24','daylight']

```

Read all 12 month data, and create a column called Month, and assign an unqiue identifier for each file when reading the data file.

After append, a list object is created, then pd.cancat creates a data frame. 

```python
list_ = []
for i, file in enumerate(files,1):
    data = pd.read_csv(file,names = col_names, low_memory=False)
    data['month'] = i 
    list_.append(data)
df_all = pd.concat(list_, ignore_index=True)

```
Create a target facility data file, convert hourly electricity data into numeric 

```python
Target =['BR3','BR4','BR5','MKR1','PH1','RB5','RL1','SH1','SH2','VVW1','VVW2','EC04','CL01']
df = df_all[df_all['AssetID'].isin(Target)]
col = ['Hour1','Hour2','Hour3','Hour4','Hour5','Hour6','Hour7','Hour8','Hour9','Hour10',
        'Hour11','Hour12','Hour13','Hour14','Hour15','Hour16','Hour17','Hour18','Hour19','Hour20',
        'Hour21','Hour22','Hour23','Hour24','daylight']

df[col] = df[col].apply(pd.to_numeric, errors = "coerce",axis = 1)
```

Create a new column to sum hourly data to daily for each facility 

```python
AESO = df.copy()
AESO['daylight'].fillna(0, inplace=True)
AESO['Total'] = AESO[col].apply(sum,axis = 1)

```
Summarized the daily total into monthly total 

```python
summary = AESO.groupby(['AssetID','month'])[['Total']].sum()
summary.to_csv('Summary_2020.csv')
```