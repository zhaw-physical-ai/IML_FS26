# dobesmic Week 1 Task 2

* Q) What was your initial question or idea?
* A) How many people were isolated (but not hospitalized) in the dataset per canton?
* Q) How did you proceed to arrive at an answer?
* A) We can use the `groupby` method to group the data by canton and then sum over the `current_isolated` column for each canton.
* Q) What are your results?
* A) Here's the following table showing the total number of people isolated (but not hospitalized) in each canton:

| abbreviation_canton_and_fl | current_isolated |
| :--- | :--- |
| AG | 690229.0 |
| AI | 19330.0 |
| AR | 24651.0 |
| BE | 2942101.0 |
| BL | 1805197.0 |
| BS | 457796.0 |
| FL | 0.0 |
| FR | 0.0 |
| GE | 2587573.0 |
| GL | 58591.0 |
| GR | 503898.0 |
| JU | 0.0 |
| LU | 1477053.0 |
| NE | 0.0 |
| NW | 85215.0 |
| OW | 76523.0 |
| SG | 1296665.0 |
| SH | 161558.0 |
| SO | 492877.0 |
| SZ | 521829.0 |
| TG | 940493.0 |
| TI | 235716.0 |
| UR | 0.0 |
| VD | 180623.0 |
| VS | 527777.0 |
| ZG | 231026.0 |
| ZH | 2977979.0 |

* Q) Include code-snippets, plots, and similar to support your answer.
* A)
```python
covid_data.groupby('abbreviation_canton_and_fl')['current_isolated'].sum()
```
