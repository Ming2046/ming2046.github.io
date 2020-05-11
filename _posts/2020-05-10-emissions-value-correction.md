---
title:  "Emissions Value Correction"
classes: wide
excerpt: "Correct emissions values from a wet basis to a dry basis at 12% CO<sub>2</sub>, 6% O<sub>2</sub> or 50% excess air"
categories: 
  - CEMS
tags:
  - Emissions Correction
mathjax: true
---

The equations are taken from [Continuous Emission Monitoring](https://www.amazon.ca/Continuous-Emission-Monitoring-James-Jahnke/dp/0471292273) by James A. Jahnke (April 3, 2000).

## Correct wet-basis concentrations to dry-basis concentrations

$$ c_d = \frac{c_w}{1-m_{Flue Gas}}  $$

where 

- $$c_d$$ = dry-basis concentration value (ppm or percent)
- $$c_w$$ = wet-basis concentration value (ppm or percent) 
- $$ m_{Flue Gas}$$ = moisture fraction of the flue gas 

To correct a concentration value for dilution, emissions can be expressed in three ways; with reference to a specified CO<sub>2</sub>, O<sub>2</sub>, or excess air value.

## CO<sub>2</sub> correction

$$ c_{d(12% CO<sub>2</sub>)} = c_w \times \frac{12}{%CO<sub>2w</sub>} $$

