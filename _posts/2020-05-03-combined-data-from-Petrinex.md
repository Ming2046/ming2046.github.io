---
title: "Combined Monthly Petrinex Data into One File"
classes: wide
excerpt: "Petrinex Data"
categories: 
  - Data Science
tags:
  - Petrinex
  - Data Science
  - Oil and Gas
---

Petrinex is a data warehouse <https://www.petrinex.ca/PD/Pages/default.aspx>. It has monthly volumetric data from Oil and Gas operations in Alberta, such as production, fuel use, flare, vent data. The volumetric data can be here <https://www.petrinex.ca/PD/Pages/APD.aspx>.

Note: data for Saskatchewan and British Columbia are not publicly available.

Check all the monthly files
```python
import pandas as pd
import numpy as np
import glob
files = glob.glob('*.csv')
files
```
Note: 
- macOS is sensitive to the letters \*\.csv or \*\.CSV. 
- Windows does not differentiate csv or CSV.



Combine all monthly files into one file

```python
df_all = pd.concat([pd.read_csv(f,low_memory=False) for f in glob.glob('*.CSV')],
                    axis = 0,sort = True)
df_all.head()
```


```python
col_removal = 
['ReportingFacilityProvinceState','ReportingFacilityLocation'
'FacilityLegalSubdivision','FacilitySection','FacilityTownship',
'FacilityRange','FacilityMeridian','SubmissionDate',
'CCICode','ProrationProduct','ProrationFactor',
'FromToIDProvinceState']
df =df_all.drop(columns= col_removal)
df.to_csv('Petrinex_2019.csv',index=False)
```
