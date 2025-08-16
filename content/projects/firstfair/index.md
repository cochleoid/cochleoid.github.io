---
title: "My First Science Fair: Acidity and Temperature"
date: 2023-02-08
draft: false
description: "From 8th grade, a project that found a roughly exponential pattern in solute data."
tags: ["projects", "nostalgia", "statistics"]
---

{{< katex >}}

# The Effect of Acidity and Temperature on Medical Solutes
**Adrian Jose Hernandez Vega**

## Abstract
The eponymous purpose of the research was to investigate the effects of acidity and temperature on medical solutes (Advil and its representations in this case). To commence, a third of the beakers were assigned a pH of 1.5 (synthesized via direct application of Sodium Bisulfate); another third, 4.5 (synthesized via dilution); and the last third, 7.5 (the unaltered pH of tap-water). The beakers were placed in pairs inside a digital thermostatic water bath, to be assessed at three different temperatures (25°C, 37°C, and 49°C) each new round; then, one pill was submerged in each beaker, and the final dissolution time (minutes) and final purity level (ppm) were recorded. There were 18 different data points in total: (Gelatin, 1.5pH, 25°C, 10 minutes), for example. Several trends were present in the data. The Tablet representations were always hastier than their Gelatin counterparts; as acidity increased, the final time decreased, as anion concentration was being altered; as temperature increased, the final time decreased, due to the endothermic net reaction. Evidenced by the corollaries in ending purity, the Gelatin Tablets make up for their relative sluggishness with their vigor, as Advil Tablets operate on the body's system "all-at-once," while Gelatin Coats operate more thoroughly. The conclusions were corroborated by the monotonic features of the bivariate exponential regressions generated from the data points: i.e., in the regressions, whenever the pH axis increased, the Time axis decreased.

## Question
How does the acidity and temperature of a liquid affect the dissolution of medications such as Advil and its variants?

## Hypothesis
As acidity increases, the medications will dissolve faster. In similar fashion, the warmer a liquid, the quicker the medications will dissolve.

## Material and Uses
- Advil Gel-Coated Pills (x9)
- Advil Tablets (x9)
- 125mL Beakers (x18)
- Nitrile Glove Pair (x2)
- Spreadsheet – Efficient data logging
- Digital Thermostatic Water Bath – To freely control temperature
- Sodium Bisulfate \( \text{(NaHSO₄)} \) – To synthesize acids
- Thermometer – To verify temperatures
- TDS Meter – To define dissolution "standard"
- pH Meter – To verify acidification levels

## Procedure
1. Prepare 18 beakers with 125 mL of tap-water. Label them as Tablet 1–9 and Gelatin 1–9.
2. Add 4g of \( \text{NaHSO₄} \) to 12 beakers (6 Tablet, 6 Gelatin) and stir to reach pH 1.5.
3. Dilute 6 of these until their pH reaches 4.5; verify with pH meter.
4. Record the purity levels of all 18 beakers.
5. Fill the thermostatic water bath and set it to 25°C; verify temperature.
6. Place a Tablet and Gelatin pair (same pH) into the bath.
7. Drop 1 Tablet and 1 Gelatin in their respective beakers and start timing.
8. Record dissolution time and final purity when each dissolves.
9. Repeat for other Tablet-Gelatin pairs at 25°C.
10. Repeat Steps 5–9 for 37°C and 49°C.

## Variables
- **Independent Variables:** Temperature, pH
- **Dependent Variable:** Dissolution time
- **Control:** Tap-water at 25°C, pH 7.5

## Data

| Presentation | Temp (°C) | pH  | Start Time     | End Time       | Elapsed Time |
|--------------|-----------|-----|----------------|----------------|---------------|
| Tablet 1     | 25        | 1.5 | 10:26:00 AM    | 10:36:00 AM    | 10 Minutes     |
| Tablet 2     | 25        | 4.5 | 06:00:00 PM    | 06:15:00 PM    | 15 Minutes     |
| Tablet 3     | 25        | 7.5 | 09:50:00 AM    | 10:20:00 AM    | 30 Minutes     |
| Tablet 4     | 37        | 1.5 | 09:46:00 PM    | 10:06:00 PM    | 20 Minutes     |
| Tablet 5     | 37        | 4.5 | 05:11:00 PM    | 05:19:00 PM    | 8 Minutes      |
| Tablet 6     | 37        | 7.5 | 01:14:00 PM    | 01:31:00 PM    | 17 Minutes     |
| Tablet 7     | 49        | 1.5 | 09:34:00 PM    | 09:39:00 PM    | 5 Minutes      |
| Tablet 8     | 49        | 4.5 | 01:27:00 PM    | 01:34:00 PM    | 7 Minutes      |
| Tablet 9     | 49        | 7.5 | 06:43:00 PM    | 06:58:00 PM    | 15 Minutes     |
| Gelatin 1    | 25        | 1.5 | 10:26:00 AM    | 01:49:00 PM    | 203 Minutes    |
| Gelatin 2    | 25        | 4.5 | 06:00:00 PM    | 06:18:00 PM    | 292 Minutes    |
| Gelatin 3    | 25        | 7.5 | 09:50:00 AM    | 11:24:00 PM    | 814 Minutes    |
| Gelatin 4    | 37        | 1.5 | 10:46:00 PM    | 11:20:00 PM    | 34 Minutes     |
| Gelatin 5    | 37        | 4.5 | 02:11:00 PM    | 02:52:00 PM    | 41 Minutes     |
| Gelatin 6    | 37        | 7.5 | 01:14:00 PM    | 05:44:00 PM    | 270 Minutes    |
| Gelatin 7    | 49        | 1.5 | 09:34:00 PM    | 09:50:00 PM    | 16 Minutes     |
| Gelatin 8    | 49        | 4.5 | 01:27:00 PM    | 01:58:00 PM    | 31 Minutes     |
| Gelatin 9    | 49        | 7.5 | 06:43:00 PM    | 07:25:00 PM    | 42 Minutes     |

## Qualitative Analysis
- Tablet versions consistently dissolve faster than Gelatin versions.
- Gelatin times vary more, suggesting inconsistency.
- Dissolution time decreases as temperature or acidity increases.
- Stomach conditions (37°C, pH 1.5) yield realistic times: ~20min for Tablets, ~34min for Gelatin.

## Statistical Analysis

| Presentation  | Average             | Median        | IQR                | Std. Dev.          |
|---------------|---------------------|---------------|---------------------|---------------------|
| Tablet (n=9)  | 14 minutes          | 15 minutes    | 11 minutes          | 15 minutes          |
| Gelatin (n=9) | 3h 14m              | 42 minutes    | 4h 9m               | 4h 17m              |
| Both (n=18)   | 1h 44m              | 25 minutes    | 27 minutes          | 3h 19m              |

## Regressional Analysis

From the data points obtained, the presence of bivariate exponential patterns was noticed. For creating a general regression, a bit of math is to be expected. We have to investigate the effect \( X \) (Temperature) and \( Y \) (pH) have on \( Z \) (Time). Two regressions were generated: one for Tablets, and one for Gelatin.

**Multiregressional Matrix Equation:**

\[
\begin{bmatrix} 
n & \sum x_i & \sum y_i \\ 
\sum x_i & \sum x_i^2 & \sum x_iy_i \\ 
\sum y_i & \sum x_iy_i & \sum y_i^2 
\end{bmatrix}
\begin{bmatrix}
\ln(a) \\
\ln(b) \\
\ln(c)
\end{bmatrix}
\]

\[=\begin{bmatrix}
\sum \ln(z_i) \\
\sum x_i\ln(z_i) \\
\sum y_i\ln(z_i)
\end{bmatrix}
\]

Substituting and solving yields:

\[
\begin{aligned}
z_T &\approx 22.3 \cdot (0.971)^x \cdot (1.12)^y \\
z_G &\approx 1590 \cdot (0.898)^x \cdot (1.28)^y
\end{aligned}
\]

## Conclusions
- The dissolution process was **endothermic**; higher temperature sped it up.
- More **acidic solutions** dissolved pills faster by affecting anion concentration.
- Realistic simulation of stomach conditions confirms product behavior.
- Purity (ppm) was a useful metric to define "fully dissolved."
- **Tablets** are best for quick relief; **Gelatin** offers a slower, more thorough release.
- The relationship between \( \text{NaHSO₄} \) and pH appeared **linear**.
