---
title:  "Emission Value Correction"
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

## CO<sub>2</sub> correction (Corrected to 12% CO<sub>2</sub>)

$$ c_{d(12\% CO_2)} = c_w \times \frac{12}{\%CO_{2w}} =c_d \times \frac{12}{\%CO_{2d}}  $$

The concentration can be determined using either a wet-basis or a dry-basis concentration value as long as the emissions and CO<sub>2</sub> are both measured on a wet basis or on a dry basis.

## O<sub>2</sub>(6% O<sub>2</sub>)

$$ c_{d(6\% O_2)} = c_d \times \frac{20.9 - 6.0}{20.9 - \%O_{2d}} $$

## Excess Air Correction 

Excess Air (EA) corrects to 50%.

$$ c_{d(50\% EA)} = c_d \times \frac{100+\%EA}{150} $$

$$ \%EA = \frac{\%O_2 - 0.5\%CO}{0.266\%N_2 - \%O_2 + 0.5\%CO} $$ 

CO% is usually negligible, this calculation requires a dry O<sub>2</sub> measurement or a wet O<sub>2</sub> measurement


