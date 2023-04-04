---
language:
- en
metrics:
- accuracy
tags:
- WildFire
---

# FireWatch Wild Fire Prediction Model
Predict wild fires based on latitude, longitude, brightness, and FRP. Input data as "latitude, longitude, brightness, FRP".

- LABEL_0 = Unlikely
- LABEL_1 = Likely

## Sample Table 

| Category | Latitude, Longitude, Brightness, FRP |
|----------|--------------------------------------|
| Likely   | -26.76123, 147.15512, 393.02, 203.63 |
| Likely   | -26.7598, 147.14514, 361.54, 79.4    |
| Unlikely | -25.70059, 149.48932, 313.9, 5.15    |
| Unlikely | -24.4318, 151.83102, 307.98, 8.79    |
| Unlikely | -23.21878, 148.91298, 314.08, 7.4    |
| Likely   | 7.87518, 19.9241, 316.32, 39.63      |
| Unlikely | -20.10942, 148.14326, 314.39, 8.8    |
| Unlikely | 7.87772, 19.9048, 304.14, 13.43      |
| Likely   | -20.79866, 124.46834, 366.74, 89.06  |
