# GeoRT Data

This directory contains the tabular data, prediction conditions, and molecular structure files used by GeoRT.

## Files

| Path | Contents |
| --- | --- |
| `thermal_conductivity_data.xlsx` | Thermal conductivity dataset read by the training configuration. The supplied configurations select the first worksheet. |
| `example_thermal_conductivity_template.csv` | Example column layout with a placeholder refrigerant and an illustrative row. |
| `r1216_conditions.csv` | Thermodynamic conditions for R1216 prediction. |
| `mol/` | 17 refrigerant molecular structures in MOL format. |

## Tabular fields

The supplied training configurations use the following column names.

| Column | Meaning |
| --- | --- |
| `name` | Refrigerant identifier used to select a molecular structure. |
| `T` | Temperature in K. |
| `p Mpa` | Pressure in MPa. Preserve this exact column spelling when using the supplied configuration. |
| `NTC` | Thermal conductivity target. Check the source dataset for its unit and scaling before adding or combining measurements. |
| `Tc` | Critical temperature in K. |
| `Pc` | Critical pressure in MPa. |
| `Tr` | Reduced temperature, T / Tc. |
| `Pr` | Reduced pressure, p / Pc. |

The R1216 conditions CSV contains `T`, `p Mpa`, `Tc`, `Pc`, `Tr`, and `Pr`. The molecular structure is supplied separately to the prediction command.

