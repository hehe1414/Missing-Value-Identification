# Missing Value Identification – Titanic Dataset

**Task 12 – Missing Value Identification**
Veda Technology | Data Analytics Track | Level 1, Day 12

## About
I checked the raw Titanic dataset (891 passengers, 12 columns) for missing values using Python and Pandas. I counted the missing values in each column, worked out the percentage, and looked at where they occur. I did not delete or change any data in this task, I only identified the missing values.

## Missing-value summary
| Column | Missing count | Missing % |
|--------|---------------|-----------|
| Cabin | 687 | 77.10% |
| Age | 177 | 19.87% |
| Embarked | 2 | 0.22% |
| All other columns (9) | 0 | 0% |

## Where the missing values occur
| Passenger class | Age missing | Cabin missing |
|-----------------|-------------|---------------|
| 1st | 30 (13.9%) | 40 (18.5%) |
| 2nd | 11 (6.0%) | 168 (91.3%) |
| 3rd | 136 (27.7%) | 479 (97.6%) |

Both passengers with a missing Embarked value were in 1st class.

## Short findings
1. **Only 3 of 12 columns have missing values.** Cabin, Age and Embarked. The other 9 columns are complete.
2. **Cabin is almost empty (77%).** It is missing for nearly all 2nd and 3rd class passengers, but for only 18.5% of 1st class passengers. So the missing values are not random: cabin records were mostly kept for first class.
3. **Age is missing for about 1 in 5 passengers (19.9%).** It is missing most often in 3rd class (27.7%) and least often in 2nd class (6.0%).
4. **Embarked has only 2 missing values (0.2%).** This is too small to matter for most analysis.

## What I would do next (not applied in this task)
| Column | Suggested action | Why |
|--------|------------------|-----|
| Cabin | Drop the column, or replace missing with "Unknown" | Too many values are missing to fill them reliably |
| Age | Fill with the median, ideally by passenger class | Deleting 177 rows would remove 20% of the data and could bias the results |
| Embarked | Fill with the most common value | Only 2 rows are affected |

I would not delete rows without a reason, because the missing values follow a pattern (for example Cabin by class), and blindly removing them could bias the analysis.

## Files
- `Missing_Values_Titanic.ipynb` – notebook with the code, output and findings
- `missing_value_summary.csv` – the summary table
- `missing_values_chart.png` – bar chart of missing % by column
- `README.md`

## Tools used
Python, Pandas, Matplotlib (Google Colab)

## Author
Rabia
