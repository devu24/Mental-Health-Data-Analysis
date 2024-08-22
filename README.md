# Mental-Health-Data-Analysis

Analyzing Students' Mental Health in SQL
In this live code-along, you'll perform exploratory data analysis on a dataset around mental health of domestic and international students. You'll perform SQL querying to look at how social connectedness and cultural issues affect mental health. Finally, you'll visualize the results of your analysis using the Python Plotly package.

The Data
This survey was conducted in 2018 at an international Japanese university and the associated study was published in 2019. It was approved by several ethical and regulatory boards.

The study found that international students have a higher risk of mental health difficulties compared to the general population, and that social connectedness and acculturative stress are predictive of depression.

Social connectedness: measure of belonging to a social group or network.

Acculturative stress: stress associated with learning about and intergrating into a new culture.

Here's an explanation for `sqldf` in Python that you can include in your GitHub README file:

---

### `sqldf` in Python

`sqldf` is a Python package that allows you to run SQL queries on pandas DataFrames. It is particularly useful when you are more comfortable with SQL or when SQL-style querying is more concise than pandas operations.

#### Key Features:
- **SQL Queries on DataFrames:** You can directly query pandas DataFrames using SQL syntax.
- **Integration with Pandas:** Leverage the power of SQL alongside pandas, making data manipulation easier and more intuitive for SQL enthusiasts.
- **Simplifies Complex Operations:** Ideal for performing complex joins, filtering, and aggregation operations that might be more verbose with pandas alone.

#### Installation:
To install `pandasql`, use pip:
```bash
pip install pandasql
```

#### Usage Example:
```python
import pandas as pd
import pandasql as ps

# Sample DataFrames
df1 = pd.DataFrame({
    'id': [1, 2, 3],
    'name': ['Alice', 'Bob', 'Charlie']
})

df2 = pd.DataFrame({
    'id': [1, 2, 3],
    'age': [25, 30, 35]
})

# SQL Query
query = '''
    SELECT df1.name, df2.age
    FROM df1
    JOIN df2 ON df1.id = df2.id
'''

# Execute Query
result = ps.sqldf(query, locals())
print(result)
```

In this example, `sqldf` allows you to perform a SQL join between two pandas DataFrames (`df1` and `df2`), returning the result as a pandas DataFrame.

#### Why Use `sqldf`?
- **SQL Familiarity:** If you are more comfortable with SQL syntax, `sqldf` offers a smooth transition to working with pandas DataFrames.
- **Cleaner Code:** For complex queries, SQL can sometimes provide a more straightforward solution than chaining multiple pandas methods.

For more details, refer to the [pandasql documentation](https://github.com/yhat/pandasql).