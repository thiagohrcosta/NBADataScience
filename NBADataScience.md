
### NBA DATAFRAME STUDY
<hr>
*A simple NBA Data used to test some Data Science concepts using Python and Pandas Library*

*Thiago H. R. Costa*
<hr>

#### 1. Shared Methods and Attributes


```python
import pandas as pd
```


```python
nba = pd.read_csv("nba.csv")
```


```python
nba.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.tail()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>453</th>
      <td>Shelvin Mack</td>
      <td>Utah Jazz</td>
      <td>8.0</td>
      <td>PG</td>
      <td>26.0</td>
      <td>6-3</td>
      <td>203.0</td>
      <td>Butler</td>
      <td>2433333.0</td>
    </tr>
    <tr>
      <th>454</th>
      <td>Raul Neto</td>
      <td>Utah Jazz</td>
      <td>25.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-1</td>
      <td>179.0</td>
      <td>NaN</td>
      <td>900000.0</td>
    </tr>
    <tr>
      <th>455</th>
      <td>Tibor Pleiss</td>
      <td>Utah Jazz</td>
      <td>21.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-3</td>
      <td>256.0</td>
      <td>NaN</td>
      <td>2900000.0</td>
    </tr>
    <tr>
      <th>456</th>
      <td>Jeff Withey</td>
      <td>Utah Jazz</td>
      <td>24.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>231.0</td>
      <td>Kansas</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.index
```




    RangeIndex(start=0, stop=458, step=1)




```python
nba.shape
```




    (458, 9)




```python
nba.dtypes
```




    Name         object
    Team         object
    Number      float64
    Position     object
    Age         float64
    Height       object
    Weight      float64
    College      object
    Salary      float64
    dtype: object




```python
nba.columns
```




    Index(['Name', 'Team', 'Number', 'Position', 'Age', 'Height', 'Weight',
           'College', 'Salary'],
          dtype='object')




```python
nba.axes
```




    [RangeIndex(start=0, stop=458, step=1),
     Index(['Name', 'Team', 'Number', 'Position', 'Age', 'Height', 'Weight',
            'College', 'Salary'],
           dtype='object')]




```python
nba.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 458 entries, 0 to 457
    Data columns (total 9 columns):
    Name        457 non-null object
    Team        457 non-null object
    Number      457 non-null float64
    Position    457 non-null object
    Age         457 non-null float64
    Height      457 non-null object
    Weight      457 non-null float64
    College     373 non-null object
    Salary      446 non-null float64
    dtypes: float64(4), object(5)
    memory usage: 32.3+ KB
    


```python
nba.get_dtype_counts()
```




    float64    4
    object     5
    dtype: int64



#### 1.1 Select One Column from a DataFrame


```python
nba.Age
```




    0      25.0
    1      25.0
    2      27.0
    3      22.0
    4      29.0
    5      29.0
    6      21.0
    7      25.0
    8      22.0
    9      22.0
    10     24.0
    11     27.0
    12     27.0
    13     20.0
    14     26.0
    15     27.0
    16     24.0
    17     28.0
    18     21.0
    19     32.0
    20     22.0
    21     26.0
    22     23.0
    23     28.0
    24     21.0
    25     26.0
    26     25.0
    27     26.0
    28     28.0
    29     27.0
           ... 
    428    25.0
    429    23.0
    430    24.0
    431    27.0
    432    23.0
    433    28.0
    434    34.0
    435    24.0
    436    25.0
    437    24.0
    438    23.0
    439    26.0
    440    30.0
    441    20.0
    442    28.0
    443    23.0
    444    24.0
    445    20.0
    446    24.0
    447    23.0
    448    26.0
    449    23.0
    450    28.0
    451    26.0
    452    20.0
    453    26.0
    454    24.0
    455    26.0
    456    26.0
    457     NaN
    Name: Age, Length: 458, dtype: float64




```python
nba.Name.head(5)
```




    0    Avery Bradley
    1      Jae Crowder
    2     John Holland
    3      R.J. Hunter
    4    Jonas Jerebko
    Name: Name, dtype: object




```python
nba["Name"]
nba["Salary"]
nba["Age"].head(3)
```




    0    25.0
    1    25.0
    2    27.0
    Name: Age, dtype: float64




```python
type(nba["Name"])
```




    pandas.core.series.Series




```python
nba["Name"].head(10)
```




    0    Avery Bradley
    1      Jae Crowder
    2     John Holland
    3      R.J. Hunter
    4    Jonas Jerebko
    5     Amir Johnson
    6    Jordan Mickey
    7     Kelly Olynyk
    8     Terry Rozier
    9     Marcus Smart
    Name: Name, dtype: object




```python
nba.head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba[ ["Name", "Team", "Age"] ].head(5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Age</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>25.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>25.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>27.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>22.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>29.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba[["Age", "Name"]]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age</th>
      <th>Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>25.0</td>
      <td>Avery Bradley</td>
    </tr>
    <tr>
      <th>1</th>
      <td>25.0</td>
      <td>Jae Crowder</td>
    </tr>
    <tr>
      <th>2</th>
      <td>27.0</td>
      <td>John Holland</td>
    </tr>
    <tr>
      <th>3</th>
      <td>22.0</td>
      <td>R.J. Hunter</td>
    </tr>
    <tr>
      <th>4</th>
      <td>29.0</td>
      <td>Jonas Jerebko</td>
    </tr>
    <tr>
      <th>5</th>
      <td>29.0</td>
      <td>Amir Johnson</td>
    </tr>
    <tr>
      <th>6</th>
      <td>21.0</td>
      <td>Jordan Mickey</td>
    </tr>
    <tr>
      <th>7</th>
      <td>25.0</td>
      <td>Kelly Olynyk</td>
    </tr>
    <tr>
      <th>8</th>
      <td>22.0</td>
      <td>Terry Rozier</td>
    </tr>
    <tr>
      <th>9</th>
      <td>22.0</td>
      <td>Marcus Smart</td>
    </tr>
    <tr>
      <th>10</th>
      <td>24.0</td>
      <td>Jared Sullinger</td>
    </tr>
    <tr>
      <th>11</th>
      <td>27.0</td>
      <td>Isaiah Thomas</td>
    </tr>
    <tr>
      <th>12</th>
      <td>27.0</td>
      <td>Evan Turner</td>
    </tr>
    <tr>
      <th>13</th>
      <td>20.0</td>
      <td>James Young</td>
    </tr>
    <tr>
      <th>14</th>
      <td>26.0</td>
      <td>Tyler Zeller</td>
    </tr>
    <tr>
      <th>15</th>
      <td>27.0</td>
      <td>Bojan Bogdanovic</td>
    </tr>
    <tr>
      <th>16</th>
      <td>24.0</td>
      <td>Markel Brown</td>
    </tr>
    <tr>
      <th>17</th>
      <td>28.0</td>
      <td>Wayne Ellington</td>
    </tr>
    <tr>
      <th>18</th>
      <td>21.0</td>
      <td>Rondae Hollis-Jefferson</td>
    </tr>
    <tr>
      <th>19</th>
      <td>32.0</td>
      <td>Jarrett Jack</td>
    </tr>
    <tr>
      <th>20</th>
      <td>22.0</td>
      <td>Sergey Karasev</td>
    </tr>
    <tr>
      <th>21</th>
      <td>26.0</td>
      <td>Sean Kilpatrick</td>
    </tr>
    <tr>
      <th>22</th>
      <td>23.0</td>
      <td>Shane Larkin</td>
    </tr>
    <tr>
      <th>23</th>
      <td>28.0</td>
      <td>Brook Lopez</td>
    </tr>
    <tr>
      <th>24</th>
      <td>21.0</td>
      <td>Chris McCullough</td>
    </tr>
    <tr>
      <th>25</th>
      <td>26.0</td>
      <td>Willie Reed</td>
    </tr>
    <tr>
      <th>26</th>
      <td>25.0</td>
      <td>Thomas Robinson</td>
    </tr>
    <tr>
      <th>27</th>
      <td>26.0</td>
      <td>Henry Sims</td>
    </tr>
    <tr>
      <th>28</th>
      <td>28.0</td>
      <td>Donald Sloan</td>
    </tr>
    <tr>
      <th>29</th>
      <td>27.0</td>
      <td>Thaddeus Young</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>428</th>
      <td>25.0</td>
      <td>Al-Farouq Aminu</td>
    </tr>
    <tr>
      <th>429</th>
      <td>23.0</td>
      <td>Pat Connaughton</td>
    </tr>
    <tr>
      <th>430</th>
      <td>24.0</td>
      <td>Allen Crabbe</td>
    </tr>
    <tr>
      <th>431</th>
      <td>27.0</td>
      <td>Ed Davis</td>
    </tr>
    <tr>
      <th>432</th>
      <td>23.0</td>
      <td>Maurice Harkless</td>
    </tr>
    <tr>
      <th>433</th>
      <td>28.0</td>
      <td>Gerald Henderson</td>
    </tr>
    <tr>
      <th>434</th>
      <td>34.0</td>
      <td>Chris Kaman</td>
    </tr>
    <tr>
      <th>435</th>
      <td>24.0</td>
      <td>Meyers Leonard</td>
    </tr>
    <tr>
      <th>436</th>
      <td>25.0</td>
      <td>Damian Lillard</td>
    </tr>
    <tr>
      <th>437</th>
      <td>24.0</td>
      <td>C.J. McCollum</td>
    </tr>
    <tr>
      <th>438</th>
      <td>23.0</td>
      <td>Luis Montero</td>
    </tr>
    <tr>
      <th>439</th>
      <td>26.0</td>
      <td>Mason Plumlee</td>
    </tr>
    <tr>
      <th>440</th>
      <td>30.0</td>
      <td>Brian Roberts</td>
    </tr>
    <tr>
      <th>441</th>
      <td>20.0</td>
      <td>Noah Vonleh</td>
    </tr>
    <tr>
      <th>442</th>
      <td>28.0</td>
      <td>Trevor Booker</td>
    </tr>
    <tr>
      <th>443</th>
      <td>23.0</td>
      <td>Trey Burke</td>
    </tr>
    <tr>
      <th>444</th>
      <td>24.0</td>
      <td>Alec Burks</td>
    </tr>
    <tr>
      <th>445</th>
      <td>20.0</td>
      <td>Dante Exum</td>
    </tr>
    <tr>
      <th>446</th>
      <td>24.0</td>
      <td>Derrick Favors</td>
    </tr>
    <tr>
      <th>447</th>
      <td>23.0</td>
      <td>Rudy Gobert</td>
    </tr>
    <tr>
      <th>448</th>
      <td>26.0</td>
      <td>Gordon Hayward</td>
    </tr>
    <tr>
      <th>449</th>
      <td>23.0</td>
      <td>Rodney Hood</td>
    </tr>
    <tr>
      <th>450</th>
      <td>28.0</td>
      <td>Joe Ingles</td>
    </tr>
    <tr>
      <th>451</th>
      <td>26.0</td>
      <td>Chris Johnson</td>
    </tr>
    <tr>
      <th>452</th>
      <td>20.0</td>
      <td>Trey Lyles</td>
    </tr>
    <tr>
      <th>453</th>
      <td>26.0</td>
      <td>Shelvin Mack</td>
    </tr>
    <tr>
      <th>454</th>
      <td>24.0</td>
      <td>Raul Neto</td>
    </tr>
    <tr>
      <th>455</th>
      <td>26.0</td>
      <td>Tibor Pleiss</td>
    </tr>
    <tr>
      <th>456</th>
      <td>26.0</td>
      <td>Jeff Withey</td>
    </tr>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>458 rows × 2 columns</p>
</div>




```python
nba[["Salary", "Team", "Name"]].tail()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Salary</th>
      <th>Team</th>
      <th>Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>453</th>
      <td>2433333.0</td>
      <td>Utah Jazz</td>
      <td>Shelvin Mack</td>
    </tr>
    <tr>
      <th>454</th>
      <td>900000.0</td>
      <td>Utah Jazz</td>
      <td>Raul Neto</td>
    </tr>
    <tr>
      <th>455</th>
      <td>2900000.0</td>
      <td>Utah Jazz</td>
      <td>Tibor Pleiss</td>
    </tr>
    <tr>
      <th>456</th>
      <td>947276.0</td>
      <td>Utah Jazz</td>
      <td>Jeff Withey</td>
    </tr>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
select = ["Salary", "Team", "Name"]
nba[select].head(5)

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Salary</th>
      <th>Team</th>
      <th>Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>7730337.0</td>
      <td>Boston Celtics</td>
      <td>Avery Bradley</td>
    </tr>
    <tr>
      <th>1</th>
      <td>6796117.0</td>
      <td>Boston Celtics</td>
      <td>Jae Crowder</td>
    </tr>
    <tr>
      <th>2</th>
      <td>NaN</td>
      <td>Boston Celtics</td>
      <td>John Holland</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1148640.0</td>
      <td>Boston Celtics</td>
      <td>R.J. Hunter</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5000000.0</td>
      <td>Boston Celtics</td>
      <td>Jonas Jerebko</td>
    </tr>
  </tbody>
</table>
</div>



#### 1.2. Add New Column to DataFrame


```python
nba["Sport"] = "Basketball"
```


```python
nba.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
      <th>Sport</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
      <td>Basketball</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
      <td>Basketball</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
      <td>Basketball</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
      <td>Basketball</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
      <td>Basketball</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba["League"] = "NBA"
```


```python
nba.head(5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
      <th>Sport</th>
      <th>League</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
      <td>Basketball</td>
      <td>NBA</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
      <td>Basketball</td>
      <td>NBA</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
      <td>Basketball</td>
      <td>NBA</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
      <td>Basketball</td>
      <td>NBA</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
      <td>Basketball</td>
      <td>NBA</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba = pd.read_csv("nba.csv")
nba.head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.insert(2, column = "Sport", value = "Basketball")
```


```python
nba.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Sport</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>Basketball</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>Basketball</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>Basketball</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>Basketball</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>Basketball</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.insert(3, column = "League", value = "NBA")
```


```python
nba.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Sport</th>
      <th>League</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>Basketball</td>
      <td>NBA</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>Basketball</td>
      <td>NBA</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>Basketball</td>
      <td>NBA</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>Basketball</td>
      <td>NBA</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>Basketball</td>
      <td>NBA</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
    </tr>
  </tbody>
</table>
</div>



#### 1.3. Broadcasting Operations


```python
nba = pd.read_csv("nba.csv")
nba.head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba["Age"].head(5)
```




    0    25.0
    1    25.0
    2    27.0
    3    22.0
    4    29.0
    Name: Age, dtype: float64




```python
nba["Age"].add(5).head(5)
```




    0    30.0
    1    30.0
    2    32.0
    3    27.0
    4    34.0
    Name: Age, dtype: float64




```python
nba["Age"] + 5
```




    0      30.0
    1      30.0
    2      32.0
    3      27.0
    4      34.0
    5      34.0
    6      26.0
    7      30.0
    8      27.0
    9      27.0
    10     29.0
    11     32.0
    12     32.0
    13     25.0
    14     31.0
    15     32.0
    16     29.0
    17     33.0
    18     26.0
    19     37.0
    20     27.0
    21     31.0
    22     28.0
    23     33.0
    24     26.0
    25     31.0
    26     30.0
    27     31.0
    28     33.0
    29     32.0
           ... 
    428    30.0
    429    28.0
    430    29.0
    431    32.0
    432    28.0
    433    33.0
    434    39.0
    435    29.0
    436    30.0
    437    29.0
    438    28.0
    439    31.0
    440    35.0
    441    25.0
    442    33.0
    443    28.0
    444    29.0
    445    25.0
    446    29.0
    447    28.0
    448    31.0
    449    28.0
    450    33.0
    451    31.0
    452    25.0
    453    31.0
    454    29.0
    455    31.0
    456    31.0
    457     NaN
    Name: Age, Length: 458, dtype: float64




```python
nba["Salary"].sub(5000000)
nba["Salary"] - 5000000

```




    0       2730337.0
    1       1796117.0
    2             NaN
    3      -3851360.0
    4             0.0
    5       7000000.0
    6      -3829040.0
    7      -2834840.0
    8      -3175640.0
    9      -1568960.0
    10     -2430740.0
    11      1912869.0
    12     -1574490.0
    13     -3250160.0
    14     -2383025.0
    15     -1574490.0
    16     -4154941.0
    17     -3500000.0
    18     -3664520.0
    19      1300000.0
    20     -3400160.0
    21     -4865785.0
    22     -3500000.0
    23     14689000.0
    24     -3859760.0
    25     -4052724.0
    26     -4018652.0
    27     -4052724.0
    28     -4052724.0
    29      6235955.0
              ...    
    428     3042895.0
    429    -4374907.0
    430    -4052724.0
    431     1980802.0
    432    -2105941.0
    433     1000000.0
    434       16000.0
    435    -1924120.0
    436     -763713.0
    437    -2474840.0
    438    -4474907.0
    439    -3584480.0
    440    -2145060.0
    441    -2362280.0
    442     -225000.0
    443    -2341760.0
    444     4463484.0
    445    -1222280.0
    446     7000000.0
    447    -3824120.0
    448    10409570.0
    449    -3651560.0
    450    -2950000.0
    451    -4018652.0
    452    -2760200.0
    453    -2566667.0
    454    -4100000.0
    455    -2100000.0
    456    -4052724.0
    457           NaN
    Name: Salary, Length: 458, dtype: float64




```python
# Convert pound to KG
nba["Weight"].mul(0.453592)
```




    0       81.646560
    1      106.594120
    2       92.986360
    3       83.914520
    4      104.779752
    5      108.862080
    6      106.594120
    7      107.954896
    8       86.182480
    9       99.790240
    10     117.933920
    11      83.914520
    12      99.790240
    13      97.522280
    14     114.758776
    15      97.975872
    16      86.182480
    17      90.718400
    18      99.790240
    19      90.718400
    20      94.347136
    21      99.336648
    22      79.378600
    23     124.737800
    24      90.718400
    25      99.790240
    26     107.501304
    27     112.490816
    28      92.986360
    29     100.243832
              ...    
    428     97.522280
    429     93.439952
    430     95.254320
    431    108.862080
    432     97.522280
    433     97.522280
    434    120.201880
    435    111.130040
    436     88.450440
    437     90.718400
    438     83.914520
    439    106.594120
    440     78.471416
    441    108.862080
    442    103.418976
    443     86.636072
    444     97.068688
    445     86.182480
    446    120.201880
    447    111.130040
    448    102.511792
    449     93.439952
    450    102.511792
    451     93.439952
    452    106.140528
    453     92.079176
    454     81.192968
    455    116.119552
    456    104.779752
    457           NaN
    Name: Weight, Length: 458, dtype: float64




```python
nba ["Weight in Kilograms"] = nba["Weight"] * 0.453592
```


```python
nba.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
      <th>Weight in Kilograms</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
      <td>81.646560</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
      <td>106.594120</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
      <td>92.986360</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
      <td>83.914520</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
      <td>104.779752</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba["Salary"].div(1000000)
```




    0       7.730337
    1       6.796117
    2            NaN
    3       1.148640
    4       5.000000
    5      12.000000
    6       1.170960
    7       2.165160
    8       1.824360
    9       3.431040
    10      2.569260
    11      6.912869
    12      3.425510
    13      1.749840
    14      2.616975
    15      3.425510
    16      0.845059
    17      1.500000
    18      1.335480
    19      6.300000
    20      1.599840
    21      0.134215
    22      1.500000
    23     19.689000
    24      1.140240
    25      0.947276
    26      0.981348
    27      0.947276
    28      0.947276
    29     11.235955
             ...    
    428     8.042895
    429     0.625093
    430     0.947276
    431     6.980802
    432     2.894059
    433     6.000000
    434     5.016000
    435     3.075880
    436     4.236287
    437     2.525160
    438     0.525093
    439     1.415520
    440     2.854940
    441     2.637720
    442     4.775000
    443     2.658240
    444     9.463484
    445     3.777720
    446    12.000000
    447     1.175880
    448    15.409570
    449     1.348440
    450     2.050000
    451     0.981348
    452     2.239800
    453     2.433333
    454     0.900000
    455     2.900000
    456     0.947276
    457          NaN
    Name: Salary, Length: 458, dtype: float64




```python
nba["Salary in Millions"] = nba["Salary"] / 1000000
```


```python
nba.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
      <th>Weight in Kilograms</th>
      <th>Salary in Millions</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
      <td>81.646560</td>
      <td>7.730337</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
      <td>106.594120</td>
      <td>6.796117</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
      <td>92.986360</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
      <td>83.914520</td>
      <td>1.148640</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
      <td>104.779752</td>
      <td>5.000000</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba = pd.read_csv("nba.csv")
nba.head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>



#### 1.4. A Review of the .value_counts(  ) Method


```python
nba["Team"].value_counts()
```




    New Orleans Pelicans      19
    Memphis Grizzlies         18
    Milwaukee Bucks           16
    New York Knicks           16
    Sacramento Kings          15
    Charlotte Hornets         15
    Portland Trail Blazers    15
    Houston Rockets           15
    Washington Wizards        15
    Utah Jazz                 15
    Toronto Raptors           15
    Golden State Warriors     15
    Los Angeles Clippers      15
    Chicago Bulls             15
    Boston Celtics            15
    Brooklyn Nets             15
    Denver Nuggets            15
    Miami Heat                15
    San Antonio Spurs         15
    Cleveland Cavaliers       15
    Dallas Mavericks          15
    Detroit Pistons           15
    Philadelphia 76ers        15
    Oklahoma City Thunder     15
    Los Angeles Lakers        15
    Phoenix Suns              15
    Indiana Pacers            15
    Atlanta Hawks             15
    Orlando Magic             14
    Minnesota Timberwolves    14
    Name: Team, dtype: int64




```python
nba["Position"].value_counts()
```




    SG    102
    PF    100
    PG     92
    SF     85
    C      78
    Name: Position, dtype: int64




```python
nba["Position"].value_counts().head(1)
```




    SG    102
    Name: Position, dtype: int64




```python
nba["Weight"].value_counts()
```




    220.0    29
    240.0    28
    250.0    26
    200.0    25
    205.0    22
    245.0    19
    235.0    17
    210.0    17
    225.0    17
    230.0    17
    185.0    16
    190.0    16
    195.0    15
    215.0    13
    175.0    12
    260.0    10
    255.0    10
    265.0     8
    228.0     7
    270.0     6
    275.0     5
    206.0     5
    189.0     4
    218.0     4
    194.0     4
    212.0     4
    180.0     4
    186.0     4
    237.0     4
    226.0     3
             ..
    207.0     1
    216.0     1
    183.0     1
    280.0     1
    256.0     1
    279.0     1
    241.0     1
    290.0     1
    244.0     1
    173.0     1
    223.0     1
    161.0     1
    221.0     1
    170.0     1
    193.0     1
    233.0     1
    188.0     1
    243.0     1
    192.0     1
    229.0     1
    249.0     1
    217.0     1
    202.0     1
    252.0     1
    254.0     1
    278.0     1
    227.0     1
    239.0     1
    289.0     1
    307.0     1
    Name: Weight, Length: 87, dtype: int64




```python
nba["Salary"].value_counts()
```




    947276.0      31
    845059.0      18
    525093.0      13
    981348.0       6
    1100602.0      5
    16407500.0     5
    5000000.0      5
    12000000.0     5
    8000000.0      5
    4000000.0      5
    3000000.0      4
    7000000.0      4
    2814000.0      4
    1000000.0      4
    19689000.0     4
    200600.0       3
    8500000.0      3
    2500000.0      3
    1015421.0      3
    2854940.0      3
    13500000.0     3
    5543725.0      3
    2288205.0      2
    1270964.0      2
    2900000.0      2
    1007026.0      2
    111444.0       2
    13000000.0     2
    1500000.0      2
    1842000.0      2
                  ..
    2239800.0      1
    1474440.0      1
    19688000.0     1
    7900000.0      1
    2008748.0      1
    13800000.0     1
    2841960.0      1
    1404600.0      1
    1584480.0      1
    273038.0       1
    9213483.0      1
    3272091.0      1
    3075880.0      1
    2250000.0      1
    4626960.0      1
    1304520.0      1
    12100000.0     1
    7500000.0      1
    295327.0       1
    2836186.0      1
    6486486.0      1
    5016000.0      1
    3333333.0      1
    1824360.0      1
    8042895.0      1
    1242720.0      1
    2489530.0      1
    5103120.0      1
    9463484.0      1
    700902.0       1
    Name: Salary, Length: 309, dtype: int64



#### 1.5. Drop Rows with Null Values


```python
nba.tail(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>455</th>
      <td>Tibor Pleiss</td>
      <td>Utah Jazz</td>
      <td>21.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-3</td>
      <td>256.0</td>
      <td>NaN</td>
      <td>2900000.0</td>
    </tr>
    <tr>
      <th>456</th>
      <td>Jeff Withey</td>
      <td>Utah Jazz</td>
      <td>24.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>231.0</td>
      <td>Kansas</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.dropna().tail(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>452</th>
      <td>Trey Lyles</td>
      <td>Utah Jazz</td>
      <td>41.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-10</td>
      <td>234.0</td>
      <td>Kentucky</td>
      <td>2239800.0</td>
    </tr>
    <tr>
      <th>453</th>
      <td>Shelvin Mack</td>
      <td>Utah Jazz</td>
      <td>8.0</td>
      <td>PG</td>
      <td>26.0</td>
      <td>6-3</td>
      <td>203.0</td>
      <td>Butler</td>
      <td>2433333.0</td>
    </tr>
    <tr>
      <th>456</th>
      <td>Jeff Withey</td>
      <td>Utah Jazz</td>
      <td>24.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>231.0</td>
      <td>Kansas</td>
      <td>947276.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.dropna(how = "all", inplace = True)
```


```python
nba.tail(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>454</th>
      <td>Raul Neto</td>
      <td>Utah Jazz</td>
      <td>25.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-1</td>
      <td>179.0</td>
      <td>NaN</td>
      <td>900000.0</td>
    </tr>
    <tr>
      <th>455</th>
      <td>Tibor Pleiss</td>
      <td>Utah Jazz</td>
      <td>21.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-3</td>
      <td>256.0</td>
      <td>NaN</td>
      <td>2900000.0</td>
    </tr>
    <tr>
      <th>456</th>
      <td>Jeff Withey</td>
      <td>Utah Jazz</td>
      <td>24.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>231.0</td>
      <td>Kansas</td>
      <td>947276.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.dropna(axis = 1).head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Amir Johnson</td>
      <td>Boston Celtics</td>
      <td>90.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-9</td>
      <td>240.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Jordan Mickey</td>
      <td>Boston Celtics</td>
      <td>55.0</td>
      <td>PF</td>
      <td>21.0</td>
      <td>6-8</td>
      <td>235.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Kelly Olynyk</td>
      <td>Boston Celtics</td>
      <td>41.0</td>
      <td>C</td>
      <td>25.0</td>
      <td>7-0</td>
      <td>238.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Terry Rozier</td>
      <td>Boston Celtics</td>
      <td>12.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-2</td>
      <td>190.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Marcus Smart</td>
      <td>Boston Celtics</td>
      <td>36.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-4</td>
      <td>220.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.dropna(subset = ["Salary"])
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Amir Johnson</td>
      <td>Boston Celtics</td>
      <td>90.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Jordan Mickey</td>
      <td>Boston Celtics</td>
      <td>55.0</td>
      <td>PF</td>
      <td>21.0</td>
      <td>6-8</td>
      <td>235.0</td>
      <td>LSU</td>
      <td>1170960.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Kelly Olynyk</td>
      <td>Boston Celtics</td>
      <td>41.0</td>
      <td>C</td>
      <td>25.0</td>
      <td>7-0</td>
      <td>238.0</td>
      <td>Gonzaga</td>
      <td>2165160.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Terry Rozier</td>
      <td>Boston Celtics</td>
      <td>12.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-2</td>
      <td>190.0</td>
      <td>Louisville</td>
      <td>1824360.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Marcus Smart</td>
      <td>Boston Celtics</td>
      <td>36.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-4</td>
      <td>220.0</td>
      <td>Oklahoma State</td>
      <td>3431040.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Jared Sullinger</td>
      <td>Boston Celtics</td>
      <td>7.0</td>
      <td>C</td>
      <td>24.0</td>
      <td>6-9</td>
      <td>260.0</td>
      <td>Ohio State</td>
      <td>2569260.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Isaiah Thomas</td>
      <td>Boston Celtics</td>
      <td>4.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>5-9</td>
      <td>185.0</td>
      <td>Washington</td>
      <td>6912869.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Evan Turner</td>
      <td>Boston Celtics</td>
      <td>11.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>Ohio State</td>
      <td>3425510.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>James Young</td>
      <td>Boston Celtics</td>
      <td>13.0</td>
      <td>SG</td>
      <td>20.0</td>
      <td>6-6</td>
      <td>215.0</td>
      <td>Kentucky</td>
      <td>1749840.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Tyler Zeller</td>
      <td>Boston Celtics</td>
      <td>44.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>253.0</td>
      <td>North Carolina</td>
      <td>2616975.0</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Bojan Bogdanovic</td>
      <td>Brooklyn Nets</td>
      <td>44.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-8</td>
      <td>216.0</td>
      <td>NaN</td>
      <td>3425510.0</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Markel Brown</td>
      <td>Brooklyn Nets</td>
      <td>22.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-3</td>
      <td>190.0</td>
      <td>Oklahoma State</td>
      <td>845059.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Wayne Ellington</td>
      <td>Brooklyn Nets</td>
      <td>21.0</td>
      <td>SG</td>
      <td>28.0</td>
      <td>6-4</td>
      <td>200.0</td>
      <td>North Carolina</td>
      <td>1500000.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Rondae Hollis-Jefferson</td>
      <td>Brooklyn Nets</td>
      <td>24.0</td>
      <td>SG</td>
      <td>21.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>Arizona</td>
      <td>1335480.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Jarrett Jack</td>
      <td>Brooklyn Nets</td>
      <td>2.0</td>
      <td>PG</td>
      <td>32.0</td>
      <td>6-3</td>
      <td>200.0</td>
      <td>Georgia Tech</td>
      <td>6300000.0</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Sergey Karasev</td>
      <td>Brooklyn Nets</td>
      <td>10.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-7</td>
      <td>208.0</td>
      <td>NaN</td>
      <td>1599840.0</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Sean Kilpatrick</td>
      <td>Brooklyn Nets</td>
      <td>6.0</td>
      <td>SG</td>
      <td>26.0</td>
      <td>6-4</td>
      <td>219.0</td>
      <td>Cincinnati</td>
      <td>134215.0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Shane Larkin</td>
      <td>Brooklyn Nets</td>
      <td>0.0</td>
      <td>PG</td>
      <td>23.0</td>
      <td>5-11</td>
      <td>175.0</td>
      <td>Miami (FL)</td>
      <td>1500000.0</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Brook Lopez</td>
      <td>Brooklyn Nets</td>
      <td>11.0</td>
      <td>C</td>
      <td>28.0</td>
      <td>7-0</td>
      <td>275.0</td>
      <td>Stanford</td>
      <td>19689000.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Chris McCullough</td>
      <td>Brooklyn Nets</td>
      <td>1.0</td>
      <td>PF</td>
      <td>21.0</td>
      <td>6-11</td>
      <td>200.0</td>
      <td>Syracuse</td>
      <td>1140240.0</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Willie Reed</td>
      <td>Brooklyn Nets</td>
      <td>33.0</td>
      <td>PF</td>
      <td>26.0</td>
      <td>6-10</td>
      <td>220.0</td>
      <td>Saint Louis</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Thomas Robinson</td>
      <td>Brooklyn Nets</td>
      <td>41.0</td>
      <td>PF</td>
      <td>25.0</td>
      <td>6-10</td>
      <td>237.0</td>
      <td>Kansas</td>
      <td>981348.0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Henry Sims</td>
      <td>Brooklyn Nets</td>
      <td>14.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>6-10</td>
      <td>248.0</td>
      <td>Georgetown</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Donald Sloan</td>
      <td>Brooklyn Nets</td>
      <td>15.0</td>
      <td>PG</td>
      <td>28.0</td>
      <td>6-3</td>
      <td>205.0</td>
      <td>Texas A&amp;M</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Thaddeus Young</td>
      <td>Brooklyn Nets</td>
      <td>30.0</td>
      <td>PF</td>
      <td>27.0</td>
      <td>6-8</td>
      <td>221.0</td>
      <td>Georgia Tech</td>
      <td>11235955.0</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Arron Afflalo</td>
      <td>New York Knicks</td>
      <td>4.0</td>
      <td>SG</td>
      <td>30.0</td>
      <td>6-5</td>
      <td>210.0</td>
      <td>UCLA</td>
      <td>8000000.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>427</th>
      <td>Cliff Alexander</td>
      <td>Portland Trail Blazers</td>
      <td>34.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-8</td>
      <td>240.0</td>
      <td>Kansas</td>
      <td>525093.0</td>
    </tr>
    <tr>
      <th>428</th>
      <td>Al-Farouq Aminu</td>
      <td>Portland Trail Blazers</td>
      <td>8.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-9</td>
      <td>215.0</td>
      <td>Wake Forest</td>
      <td>8042895.0</td>
    </tr>
    <tr>
      <th>429</th>
      <td>Pat Connaughton</td>
      <td>Portland Trail Blazers</td>
      <td>5.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-5</td>
      <td>206.0</td>
      <td>Notre Dame</td>
      <td>625093.0</td>
    </tr>
    <tr>
      <th>430</th>
      <td>Allen Crabbe</td>
      <td>Portland Trail Blazers</td>
      <td>23.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-6</td>
      <td>210.0</td>
      <td>California</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>431</th>
      <td>Ed Davis</td>
      <td>Portland Trail Blazers</td>
      <td>17.0</td>
      <td>C</td>
      <td>27.0</td>
      <td>6-10</td>
      <td>240.0</td>
      <td>North Carolina</td>
      <td>6980802.0</td>
    </tr>
    <tr>
      <th>432</th>
      <td>Maurice Harkless</td>
      <td>Portland Trail Blazers</td>
      <td>4.0</td>
      <td>SF</td>
      <td>23.0</td>
      <td>6-9</td>
      <td>215.0</td>
      <td>St. John's</td>
      <td>2894059.0</td>
    </tr>
    <tr>
      <th>433</th>
      <td>Gerald Henderson</td>
      <td>Portland Trail Blazers</td>
      <td>9.0</td>
      <td>SG</td>
      <td>28.0</td>
      <td>6-5</td>
      <td>215.0</td>
      <td>Duke</td>
      <td>6000000.0</td>
    </tr>
    <tr>
      <th>434</th>
      <td>Chris Kaman</td>
      <td>Portland Trail Blazers</td>
      <td>35.0</td>
      <td>C</td>
      <td>34.0</td>
      <td>7-0</td>
      <td>265.0</td>
      <td>Central Michigan</td>
      <td>5016000.0</td>
    </tr>
    <tr>
      <th>435</th>
      <td>Meyers Leonard</td>
      <td>Portland Trail Blazers</td>
      <td>11.0</td>
      <td>PF</td>
      <td>24.0</td>
      <td>7-1</td>
      <td>245.0</td>
      <td>Illinois</td>
      <td>3075880.0</td>
    </tr>
    <tr>
      <th>436</th>
      <td>Damian Lillard</td>
      <td>Portland Trail Blazers</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-3</td>
      <td>195.0</td>
      <td>Weber State</td>
      <td>4236287.0</td>
    </tr>
    <tr>
      <th>437</th>
      <td>C.J. McCollum</td>
      <td>Portland Trail Blazers</td>
      <td>3.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-4</td>
      <td>200.0</td>
      <td>Lehigh</td>
      <td>2525160.0</td>
    </tr>
    <tr>
      <th>438</th>
      <td>Luis Montero</td>
      <td>Portland Trail Blazers</td>
      <td>44.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-7</td>
      <td>185.0</td>
      <td>Westchester CC</td>
      <td>525093.0</td>
    </tr>
    <tr>
      <th>439</th>
      <td>Mason Plumlee</td>
      <td>Portland Trail Blazers</td>
      <td>24.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>6-11</td>
      <td>235.0</td>
      <td>Duke</td>
      <td>1415520.0</td>
    </tr>
    <tr>
      <th>440</th>
      <td>Brian Roberts</td>
      <td>Portland Trail Blazers</td>
      <td>2.0</td>
      <td>PG</td>
      <td>30.0</td>
      <td>6-1</td>
      <td>173.0</td>
      <td>Dayton</td>
      <td>2854940.0</td>
    </tr>
    <tr>
      <th>441</th>
      <td>Noah Vonleh</td>
      <td>Portland Trail Blazers</td>
      <td>21.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>Indiana</td>
      <td>2637720.0</td>
    </tr>
    <tr>
      <th>442</th>
      <td>Trevor Booker</td>
      <td>Utah Jazz</td>
      <td>33.0</td>
      <td>PF</td>
      <td>28.0</td>
      <td>6-8</td>
      <td>228.0</td>
      <td>Clemson</td>
      <td>4775000.0</td>
    </tr>
    <tr>
      <th>443</th>
      <td>Trey Burke</td>
      <td>Utah Jazz</td>
      <td>3.0</td>
      <td>PG</td>
      <td>23.0</td>
      <td>6-1</td>
      <td>191.0</td>
      <td>Michigan</td>
      <td>2658240.0</td>
    </tr>
    <tr>
      <th>444</th>
      <td>Alec Burks</td>
      <td>Utah Jazz</td>
      <td>10.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-6</td>
      <td>214.0</td>
      <td>Colorado</td>
      <td>9463484.0</td>
    </tr>
    <tr>
      <th>445</th>
      <td>Dante Exum</td>
      <td>Utah Jazz</td>
      <td>11.0</td>
      <td>PG</td>
      <td>20.0</td>
      <td>6-6</td>
      <td>190.0</td>
      <td>NaN</td>
      <td>3777720.0</td>
    </tr>
    <tr>
      <th>446</th>
      <td>Derrick Favors</td>
      <td>Utah Jazz</td>
      <td>15.0</td>
      <td>PF</td>
      <td>24.0</td>
      <td>6-10</td>
      <td>265.0</td>
      <td>Georgia Tech</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>447</th>
      <td>Rudy Gobert</td>
      <td>Utah Jazz</td>
      <td>27.0</td>
      <td>C</td>
      <td>23.0</td>
      <td>7-1</td>
      <td>245.0</td>
      <td>NaN</td>
      <td>1175880.0</td>
    </tr>
    <tr>
      <th>448</th>
      <td>Gordon Hayward</td>
      <td>Utah Jazz</td>
      <td>20.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-8</td>
      <td>226.0</td>
      <td>Butler</td>
      <td>15409570.0</td>
    </tr>
    <tr>
      <th>449</th>
      <td>Rodney Hood</td>
      <td>Utah Jazz</td>
      <td>5.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-8</td>
      <td>206.0</td>
      <td>Duke</td>
      <td>1348440.0</td>
    </tr>
    <tr>
      <th>450</th>
      <td>Joe Ingles</td>
      <td>Utah Jazz</td>
      <td>2.0</td>
      <td>SF</td>
      <td>28.0</td>
      <td>6-8</td>
      <td>226.0</td>
      <td>NaN</td>
      <td>2050000.0</td>
    </tr>
    <tr>
      <th>451</th>
      <td>Chris Johnson</td>
      <td>Utah Jazz</td>
      <td>23.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-6</td>
      <td>206.0</td>
      <td>Dayton</td>
      <td>981348.0</td>
    </tr>
    <tr>
      <th>452</th>
      <td>Trey Lyles</td>
      <td>Utah Jazz</td>
      <td>41.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-10</td>
      <td>234.0</td>
      <td>Kentucky</td>
      <td>2239800.0</td>
    </tr>
    <tr>
      <th>453</th>
      <td>Shelvin Mack</td>
      <td>Utah Jazz</td>
      <td>8.0</td>
      <td>PG</td>
      <td>26.0</td>
      <td>6-3</td>
      <td>203.0</td>
      <td>Butler</td>
      <td>2433333.0</td>
    </tr>
    <tr>
      <th>454</th>
      <td>Raul Neto</td>
      <td>Utah Jazz</td>
      <td>25.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-1</td>
      <td>179.0</td>
      <td>NaN</td>
      <td>900000.0</td>
    </tr>
    <tr>
      <th>455</th>
      <td>Tibor Pleiss</td>
      <td>Utah Jazz</td>
      <td>21.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-3</td>
      <td>256.0</td>
      <td>NaN</td>
      <td>2900000.0</td>
    </tr>
    <tr>
      <th>456</th>
      <td>Jeff Withey</td>
      <td>Utah Jazz</td>
      <td>24.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>231.0</td>
      <td>Kansas</td>
      <td>947276.0</td>
    </tr>
  </tbody>
</table>
<p>446 rows × 9 columns</p>
</div>




```python
nba.dropna(subset = ["Salary", "College"])
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Jordan Mickey</td>
      <td>Boston Celtics</td>
      <td>55.0</td>
      <td>PF</td>
      <td>21.0</td>
      <td>6-8</td>
      <td>235.0</td>
      <td>LSU</td>
      <td>1170960.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Kelly Olynyk</td>
      <td>Boston Celtics</td>
      <td>41.0</td>
      <td>C</td>
      <td>25.0</td>
      <td>7-0</td>
      <td>238.0</td>
      <td>Gonzaga</td>
      <td>2165160.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Terry Rozier</td>
      <td>Boston Celtics</td>
      <td>12.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-2</td>
      <td>190.0</td>
      <td>Louisville</td>
      <td>1824360.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Marcus Smart</td>
      <td>Boston Celtics</td>
      <td>36.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-4</td>
      <td>220.0</td>
      <td>Oklahoma State</td>
      <td>3431040.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Jared Sullinger</td>
      <td>Boston Celtics</td>
      <td>7.0</td>
      <td>C</td>
      <td>24.0</td>
      <td>6-9</td>
      <td>260.0</td>
      <td>Ohio State</td>
      <td>2569260.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Isaiah Thomas</td>
      <td>Boston Celtics</td>
      <td>4.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>5-9</td>
      <td>185.0</td>
      <td>Washington</td>
      <td>6912869.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Evan Turner</td>
      <td>Boston Celtics</td>
      <td>11.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>Ohio State</td>
      <td>3425510.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>James Young</td>
      <td>Boston Celtics</td>
      <td>13.0</td>
      <td>SG</td>
      <td>20.0</td>
      <td>6-6</td>
      <td>215.0</td>
      <td>Kentucky</td>
      <td>1749840.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Tyler Zeller</td>
      <td>Boston Celtics</td>
      <td>44.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>253.0</td>
      <td>North Carolina</td>
      <td>2616975.0</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Markel Brown</td>
      <td>Brooklyn Nets</td>
      <td>22.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-3</td>
      <td>190.0</td>
      <td>Oklahoma State</td>
      <td>845059.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Wayne Ellington</td>
      <td>Brooklyn Nets</td>
      <td>21.0</td>
      <td>SG</td>
      <td>28.0</td>
      <td>6-4</td>
      <td>200.0</td>
      <td>North Carolina</td>
      <td>1500000.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Rondae Hollis-Jefferson</td>
      <td>Brooklyn Nets</td>
      <td>24.0</td>
      <td>SG</td>
      <td>21.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>Arizona</td>
      <td>1335480.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Jarrett Jack</td>
      <td>Brooklyn Nets</td>
      <td>2.0</td>
      <td>PG</td>
      <td>32.0</td>
      <td>6-3</td>
      <td>200.0</td>
      <td>Georgia Tech</td>
      <td>6300000.0</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Sean Kilpatrick</td>
      <td>Brooklyn Nets</td>
      <td>6.0</td>
      <td>SG</td>
      <td>26.0</td>
      <td>6-4</td>
      <td>219.0</td>
      <td>Cincinnati</td>
      <td>134215.0</td>
    </tr>
    <tr>
      <th>22</th>
      <td>Shane Larkin</td>
      <td>Brooklyn Nets</td>
      <td>0.0</td>
      <td>PG</td>
      <td>23.0</td>
      <td>5-11</td>
      <td>175.0</td>
      <td>Miami (FL)</td>
      <td>1500000.0</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Brook Lopez</td>
      <td>Brooklyn Nets</td>
      <td>11.0</td>
      <td>C</td>
      <td>28.0</td>
      <td>7-0</td>
      <td>275.0</td>
      <td>Stanford</td>
      <td>19689000.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Chris McCullough</td>
      <td>Brooklyn Nets</td>
      <td>1.0</td>
      <td>PF</td>
      <td>21.0</td>
      <td>6-11</td>
      <td>200.0</td>
      <td>Syracuse</td>
      <td>1140240.0</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Willie Reed</td>
      <td>Brooklyn Nets</td>
      <td>33.0</td>
      <td>PF</td>
      <td>26.0</td>
      <td>6-10</td>
      <td>220.0</td>
      <td>Saint Louis</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Thomas Robinson</td>
      <td>Brooklyn Nets</td>
      <td>41.0</td>
      <td>PF</td>
      <td>25.0</td>
      <td>6-10</td>
      <td>237.0</td>
      <td>Kansas</td>
      <td>981348.0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Henry Sims</td>
      <td>Brooklyn Nets</td>
      <td>14.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>6-10</td>
      <td>248.0</td>
      <td>Georgetown</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Donald Sloan</td>
      <td>Brooklyn Nets</td>
      <td>15.0</td>
      <td>PG</td>
      <td>28.0</td>
      <td>6-3</td>
      <td>205.0</td>
      <td>Texas A&amp;M</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>29</th>
      <td>Thaddeus Young</td>
      <td>Brooklyn Nets</td>
      <td>30.0</td>
      <td>PF</td>
      <td>27.0</td>
      <td>6-8</td>
      <td>221.0</td>
      <td>Georgia Tech</td>
      <td>11235955.0</td>
    </tr>
    <tr>
      <th>30</th>
      <td>Arron Afflalo</td>
      <td>New York Knicks</td>
      <td>4.0</td>
      <td>SG</td>
      <td>30.0</td>
      <td>6-5</td>
      <td>210.0</td>
      <td>UCLA</td>
      <td>8000000.0</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Lou Amundson</td>
      <td>New York Knicks</td>
      <td>17.0</td>
      <td>PF</td>
      <td>33.0</td>
      <td>6-9</td>
      <td>220.0</td>
      <td>UNLV</td>
      <td>1635476.0</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Carmelo Anthony</td>
      <td>New York Knicks</td>
      <td>7.0</td>
      <td>SF</td>
      <td>32.0</td>
      <td>6-8</td>
      <td>240.0</td>
      <td>Syracuse</td>
      <td>22875000.0</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Cleanthony Early</td>
      <td>New York Knicks</td>
      <td>11.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-8</td>
      <td>210.0</td>
      <td>Wichita State</td>
      <td>845059.0</td>
    </tr>
    <tr>
      <th>36</th>
      <td>Langston Galloway</td>
      <td>New York Knicks</td>
      <td>2.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-2</td>
      <td>200.0</td>
      <td>Saint Joseph's</td>
      <td>845059.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>422</th>
      <td>Cameron Payne</td>
      <td>Oklahoma City Thunder</td>
      <td>22.0</td>
      <td>PG</td>
      <td>21.0</td>
      <td>6-3</td>
      <td>185.0</td>
      <td>Murray State</td>
      <td>2021520.0</td>
    </tr>
    <tr>
      <th>423</th>
      <td>Andre Roberson</td>
      <td>Oklahoma City Thunder</td>
      <td>21.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-7</td>
      <td>210.0</td>
      <td>Colorado</td>
      <td>1210800.0</td>
    </tr>
    <tr>
      <th>424</th>
      <td>Kyle Singler</td>
      <td>Oklahoma City Thunder</td>
      <td>5.0</td>
      <td>SF</td>
      <td>28.0</td>
      <td>6-8</td>
      <td>228.0</td>
      <td>Duke</td>
      <td>4500000.0</td>
    </tr>
    <tr>
      <th>425</th>
      <td>Dion Waiters</td>
      <td>Oklahoma City Thunder</td>
      <td>3.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-4</td>
      <td>220.0</td>
      <td>Syracuse</td>
      <td>5138430.0</td>
    </tr>
    <tr>
      <th>426</th>
      <td>Russell Westbrook</td>
      <td>Oklahoma City Thunder</td>
      <td>0.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-3</td>
      <td>200.0</td>
      <td>UCLA</td>
      <td>16744218.0</td>
    </tr>
    <tr>
      <th>427</th>
      <td>Cliff Alexander</td>
      <td>Portland Trail Blazers</td>
      <td>34.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-8</td>
      <td>240.0</td>
      <td>Kansas</td>
      <td>525093.0</td>
    </tr>
    <tr>
      <th>428</th>
      <td>Al-Farouq Aminu</td>
      <td>Portland Trail Blazers</td>
      <td>8.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-9</td>
      <td>215.0</td>
      <td>Wake Forest</td>
      <td>8042895.0</td>
    </tr>
    <tr>
      <th>429</th>
      <td>Pat Connaughton</td>
      <td>Portland Trail Blazers</td>
      <td>5.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-5</td>
      <td>206.0</td>
      <td>Notre Dame</td>
      <td>625093.0</td>
    </tr>
    <tr>
      <th>430</th>
      <td>Allen Crabbe</td>
      <td>Portland Trail Blazers</td>
      <td>23.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-6</td>
      <td>210.0</td>
      <td>California</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>431</th>
      <td>Ed Davis</td>
      <td>Portland Trail Blazers</td>
      <td>17.0</td>
      <td>C</td>
      <td>27.0</td>
      <td>6-10</td>
      <td>240.0</td>
      <td>North Carolina</td>
      <td>6980802.0</td>
    </tr>
    <tr>
      <th>432</th>
      <td>Maurice Harkless</td>
      <td>Portland Trail Blazers</td>
      <td>4.0</td>
      <td>SF</td>
      <td>23.0</td>
      <td>6-9</td>
      <td>215.0</td>
      <td>St. John's</td>
      <td>2894059.0</td>
    </tr>
    <tr>
      <th>433</th>
      <td>Gerald Henderson</td>
      <td>Portland Trail Blazers</td>
      <td>9.0</td>
      <td>SG</td>
      <td>28.0</td>
      <td>6-5</td>
      <td>215.0</td>
      <td>Duke</td>
      <td>6000000.0</td>
    </tr>
    <tr>
      <th>434</th>
      <td>Chris Kaman</td>
      <td>Portland Trail Blazers</td>
      <td>35.0</td>
      <td>C</td>
      <td>34.0</td>
      <td>7-0</td>
      <td>265.0</td>
      <td>Central Michigan</td>
      <td>5016000.0</td>
    </tr>
    <tr>
      <th>435</th>
      <td>Meyers Leonard</td>
      <td>Portland Trail Blazers</td>
      <td>11.0</td>
      <td>PF</td>
      <td>24.0</td>
      <td>7-1</td>
      <td>245.0</td>
      <td>Illinois</td>
      <td>3075880.0</td>
    </tr>
    <tr>
      <th>436</th>
      <td>Damian Lillard</td>
      <td>Portland Trail Blazers</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-3</td>
      <td>195.0</td>
      <td>Weber State</td>
      <td>4236287.0</td>
    </tr>
    <tr>
      <th>437</th>
      <td>C.J. McCollum</td>
      <td>Portland Trail Blazers</td>
      <td>3.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-4</td>
      <td>200.0</td>
      <td>Lehigh</td>
      <td>2525160.0</td>
    </tr>
    <tr>
      <th>438</th>
      <td>Luis Montero</td>
      <td>Portland Trail Blazers</td>
      <td>44.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-7</td>
      <td>185.0</td>
      <td>Westchester CC</td>
      <td>525093.0</td>
    </tr>
    <tr>
      <th>439</th>
      <td>Mason Plumlee</td>
      <td>Portland Trail Blazers</td>
      <td>24.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>6-11</td>
      <td>235.0</td>
      <td>Duke</td>
      <td>1415520.0</td>
    </tr>
    <tr>
      <th>440</th>
      <td>Brian Roberts</td>
      <td>Portland Trail Blazers</td>
      <td>2.0</td>
      <td>PG</td>
      <td>30.0</td>
      <td>6-1</td>
      <td>173.0</td>
      <td>Dayton</td>
      <td>2854940.0</td>
    </tr>
    <tr>
      <th>441</th>
      <td>Noah Vonleh</td>
      <td>Portland Trail Blazers</td>
      <td>21.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>Indiana</td>
      <td>2637720.0</td>
    </tr>
    <tr>
      <th>442</th>
      <td>Trevor Booker</td>
      <td>Utah Jazz</td>
      <td>33.0</td>
      <td>PF</td>
      <td>28.0</td>
      <td>6-8</td>
      <td>228.0</td>
      <td>Clemson</td>
      <td>4775000.0</td>
    </tr>
    <tr>
      <th>443</th>
      <td>Trey Burke</td>
      <td>Utah Jazz</td>
      <td>3.0</td>
      <td>PG</td>
      <td>23.0</td>
      <td>6-1</td>
      <td>191.0</td>
      <td>Michigan</td>
      <td>2658240.0</td>
    </tr>
    <tr>
      <th>444</th>
      <td>Alec Burks</td>
      <td>Utah Jazz</td>
      <td>10.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-6</td>
      <td>214.0</td>
      <td>Colorado</td>
      <td>9463484.0</td>
    </tr>
    <tr>
      <th>446</th>
      <td>Derrick Favors</td>
      <td>Utah Jazz</td>
      <td>15.0</td>
      <td>PF</td>
      <td>24.0</td>
      <td>6-10</td>
      <td>265.0</td>
      <td>Georgia Tech</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>448</th>
      <td>Gordon Hayward</td>
      <td>Utah Jazz</td>
      <td>20.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-8</td>
      <td>226.0</td>
      <td>Butler</td>
      <td>15409570.0</td>
    </tr>
    <tr>
      <th>449</th>
      <td>Rodney Hood</td>
      <td>Utah Jazz</td>
      <td>5.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-8</td>
      <td>206.0</td>
      <td>Duke</td>
      <td>1348440.0</td>
    </tr>
    <tr>
      <th>451</th>
      <td>Chris Johnson</td>
      <td>Utah Jazz</td>
      <td>23.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-6</td>
      <td>206.0</td>
      <td>Dayton</td>
      <td>981348.0</td>
    </tr>
    <tr>
      <th>452</th>
      <td>Trey Lyles</td>
      <td>Utah Jazz</td>
      <td>41.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-10</td>
      <td>234.0</td>
      <td>Kentucky</td>
      <td>2239800.0</td>
    </tr>
    <tr>
      <th>453</th>
      <td>Shelvin Mack</td>
      <td>Utah Jazz</td>
      <td>8.0</td>
      <td>PG</td>
      <td>26.0</td>
      <td>6-3</td>
      <td>203.0</td>
      <td>Butler</td>
      <td>2433333.0</td>
    </tr>
    <tr>
      <th>456</th>
      <td>Jeff Withey</td>
      <td>Utah Jazz</td>
      <td>24.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>231.0</td>
      <td>Kansas</td>
      <td>947276.0</td>
    </tr>
  </tbody>
</table>
<p>364 rows × 9 columns</p>
</div>



#### 1.6. Fill in Null Values with the .fillna(   ) Method


```python
nba = pd.read_csv("nba.csv")
nba.head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.fillna(0).head(20)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>0</td>
      <td>5000000.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Amir Johnson</td>
      <td>Boston Celtics</td>
      <td>90.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>0</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Jordan Mickey</td>
      <td>Boston Celtics</td>
      <td>55.0</td>
      <td>PF</td>
      <td>21.0</td>
      <td>6-8</td>
      <td>235.0</td>
      <td>LSU</td>
      <td>1170960.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Kelly Olynyk</td>
      <td>Boston Celtics</td>
      <td>41.0</td>
      <td>C</td>
      <td>25.0</td>
      <td>7-0</td>
      <td>238.0</td>
      <td>Gonzaga</td>
      <td>2165160.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Terry Rozier</td>
      <td>Boston Celtics</td>
      <td>12.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-2</td>
      <td>190.0</td>
      <td>Louisville</td>
      <td>1824360.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Marcus Smart</td>
      <td>Boston Celtics</td>
      <td>36.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-4</td>
      <td>220.0</td>
      <td>Oklahoma State</td>
      <td>3431040.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Jared Sullinger</td>
      <td>Boston Celtics</td>
      <td>7.0</td>
      <td>C</td>
      <td>24.0</td>
      <td>6-9</td>
      <td>260.0</td>
      <td>Ohio State</td>
      <td>2569260.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Isaiah Thomas</td>
      <td>Boston Celtics</td>
      <td>4.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>5-9</td>
      <td>185.0</td>
      <td>Washington</td>
      <td>6912869.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Evan Turner</td>
      <td>Boston Celtics</td>
      <td>11.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>Ohio State</td>
      <td>3425510.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>James Young</td>
      <td>Boston Celtics</td>
      <td>13.0</td>
      <td>SG</td>
      <td>20.0</td>
      <td>6-6</td>
      <td>215.0</td>
      <td>Kentucky</td>
      <td>1749840.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Tyler Zeller</td>
      <td>Boston Celtics</td>
      <td>44.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>253.0</td>
      <td>North Carolina</td>
      <td>2616975.0</td>
    </tr>
    <tr>
      <th>15</th>
      <td>Bojan Bogdanovic</td>
      <td>Brooklyn Nets</td>
      <td>44.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-8</td>
      <td>216.0</td>
      <td>0</td>
      <td>3425510.0</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Markel Brown</td>
      <td>Brooklyn Nets</td>
      <td>22.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-3</td>
      <td>190.0</td>
      <td>Oklahoma State</td>
      <td>845059.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Wayne Ellington</td>
      <td>Brooklyn Nets</td>
      <td>21.0</td>
      <td>SG</td>
      <td>28.0</td>
      <td>6-4</td>
      <td>200.0</td>
      <td>North Carolina</td>
      <td>1500000.0</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Rondae Hollis-Jefferson</td>
      <td>Brooklyn Nets</td>
      <td>24.0</td>
      <td>SG</td>
      <td>21.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>Arizona</td>
      <td>1335480.0</td>
    </tr>
    <tr>
      <th>19</th>
      <td>Jarrett Jack</td>
      <td>Brooklyn Nets</td>
      <td>2.0</td>
      <td>PG</td>
      <td>32.0</td>
      <td>6-3</td>
      <td>200.0</td>
      <td>Georgia Tech</td>
      <td>6300000.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba["Salary"].fillna(0, inplace = True)
```


```python
nba.head(5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba["College"].fillna("No College", inplace = True)
```


```python
nba.head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>No College</td>
      <td>5000000.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Amir Johnson</td>
      <td>Boston Celtics</td>
      <td>90.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>No College</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Jordan Mickey</td>
      <td>Boston Celtics</td>
      <td>55.0</td>
      <td>PF</td>
      <td>21.0</td>
      <td>6-8</td>
      <td>235.0</td>
      <td>LSU</td>
      <td>1170960.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Kelly Olynyk</td>
      <td>Boston Celtics</td>
      <td>41.0</td>
      <td>C</td>
      <td>25.0</td>
      <td>7-0</td>
      <td>238.0</td>
      <td>Gonzaga</td>
      <td>2165160.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Terry Rozier</td>
      <td>Boston Celtics</td>
      <td>12.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-2</td>
      <td>190.0</td>
      <td>Louisville</td>
      <td>1824360.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Marcus Smart</td>
      <td>Boston Celtics</td>
      <td>36.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-4</td>
      <td>220.0</td>
      <td>Oklahoma State</td>
      <td>3431040.0</td>
    </tr>
  </tbody>
</table>
</div>



#### 1.7. The  .astype (  ) Method


```python
nba = pd.read_csv("nba.csv").dropna(how = "all")
nba["Salary"].fillna(0, inplace = True)
nba["College"].fillna("None", inplace = True)
nba.head(6)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>None</td>
      <td>5000000.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Amir Johnson</td>
      <td>Boston Celtics</td>
      <td>90.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>None</td>
      <td>12000000.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.dtypes
nba.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 457 entries, 0 to 456
    Data columns (total 9 columns):
    Name        457 non-null object
    Team        457 non-null object
    Number      457 non-null float64
    Position    457 non-null object
    Age         457 non-null float64
    Height      457 non-null object
    Weight      457 non-null float64
    College     457 non-null object
    Salary      457 non-null float64
    dtypes: float64(4), object(5)
    memory usage: 35.7+ KB
    


```python
nba["Salary"] = nba["Salary"].astype("int")
```


```python
nba.head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba["Age"] = nba["Age"].astype("int")
nba["Number"] = nba["Number"].astype("int")
nba.head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0</td>
      <td>PG</td>
      <td>25</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99</td>
      <td>SF</td>
      <td>25</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30</td>
      <td>SG</td>
      <td>27</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba["Position"].nunique()
```




    5




```python
# Decreasing memory use
nba["Position"] = nba["Position"].astype("category")
```


```python
# Now the momory goes to 35.7Kb to 27.4Kb
nba.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 457 entries, 0 to 456
    Data columns (total 9 columns):
    Name        457 non-null object
    Team        457 non-null object
    Number      457 non-null int32
    Position    457 non-null category
    Age         457 non-null int32
    Height      457 non-null object
    Weight      457 non-null float64
    College     457 non-null object
    Salary      457 non-null int32
    dtypes: category(1), float64(1), int32(3), object(4)
    memory usage: 27.4+ KB
    


```python
# Decreasing the memory use
nba["Team"] = nba["Team"].astype("category")
```


```python
# Memory use decrease to 25.8Kb
nba.info()
```

    <class 'pandas.core.frame.DataFrame'>
    Int64Index: 457 entries, 0 to 456
    Data columns (total 9 columns):
    Name        457 non-null object
    Team        457 non-null category
    Number      457 non-null int32
    Position    457 non-null category
    Age         457 non-null int32
    Height      457 non-null object
    Weight      457 non-null float64
    College     457 non-null object
    Salary      457 non-null int32
    dtypes: category(2), float64(1), int32(3), object(3)
    memory usage: 25.8+ KB
    

#### 1.8. Sort a Data Frames with the .sort_values (   ), Method, Part I


```python
nba = pd.read_csv("nba.csv")
nba.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.sort_values("Name", ascending = False)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>237</th>
      <td>Zaza Pachulia</td>
      <td>Dallas Mavericks</td>
      <td>27.0</td>
      <td>C</td>
      <td>32.0</td>
      <td>6-11</td>
      <td>275.0</td>
      <td>NaN</td>
      <td>5200000.0</td>
    </tr>
    <tr>
      <th>271</th>
      <td>Zach Randolph</td>
      <td>Memphis Grizzlies</td>
      <td>50.0</td>
      <td>PF</td>
      <td>34.0</td>
      <td>6-9</td>
      <td>260.0</td>
      <td>Michigan State</td>
      <td>9638555.0</td>
    </tr>
    <tr>
      <th>402</th>
      <td>Zach LaVine</td>
      <td>Minnesota Timberwolves</td>
      <td>8.0</td>
      <td>PG</td>
      <td>21.0</td>
      <td>6-5</td>
      <td>189.0</td>
      <td>UCLA</td>
      <td>2148360.0</td>
    </tr>
    <tr>
      <th>270</th>
      <td>Xavier Munford</td>
      <td>Memphis Grizzlies</td>
      <td>14.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-3</td>
      <td>180.0</td>
      <td>Rhode Island</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>386</th>
      <td>Wilson Chandler</td>
      <td>Denver Nuggets</td>
      <td>21.0</td>
      <td>SF</td>
      <td>29.0</td>
      <td>6-8</td>
      <td>225.0</td>
      <td>DePaul</td>
      <td>10449438.0</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Willie Reed</td>
      <td>Brooklyn Nets</td>
      <td>33.0</td>
      <td>PF</td>
      <td>26.0</td>
      <td>6-10</td>
      <td>220.0</td>
      <td>Saint Louis</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>141</th>
      <td>Willie Cauley-Stein</td>
      <td>Sacramento Kings</td>
      <td>0.0</td>
      <td>C</td>
      <td>22.0</td>
      <td>7-0</td>
      <td>240.0</td>
      <td>Kentucky</td>
      <td>3398280.0</td>
    </tr>
    <tr>
      <th>385</th>
      <td>Will Barton</td>
      <td>Denver Nuggets</td>
      <td>5.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>175.0</td>
      <td>Memphis</td>
      <td>3533333.0</td>
    </tr>
    <tr>
      <th>233</th>
      <td>Wesley Matthews</td>
      <td>Dallas Mavericks</td>
      <td>23.0</td>
      <td>SG</td>
      <td>29.0</td>
      <td>6-5</td>
      <td>220.0</td>
      <td>Marquette</td>
      <td>16407500.0</td>
    </tr>
    <tr>
      <th>97</th>
      <td>Wesley Johnson</td>
      <td>Los Angeles Clippers</td>
      <td>33.0</td>
      <td>SF</td>
      <td>28.0</td>
      <td>6-7</td>
      <td>215.0</td>
      <td>Syracuse</td>
      <td>1100602.0</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Wayne Ellington</td>
      <td>Brooklyn Nets</td>
      <td>21.0</td>
      <td>SG</td>
      <td>28.0</td>
      <td>6-4</td>
      <td>200.0</td>
      <td>North Carolina</td>
      <td>1500000.0</td>
    </tr>
    <tr>
      <th>322</th>
      <td>Walter Tavares</td>
      <td>Atlanta Hawks</td>
      <td>22.0</td>
      <td>C</td>
      <td>24.0</td>
      <td>7-3</td>
      <td>260.0</td>
      <td>NaN</td>
      <td>1000000.0</td>
    </tr>
    <tr>
      <th>261</th>
      <td>Vince Carter</td>
      <td>Memphis Grizzlies</td>
      <td>15.0</td>
      <td>SG</td>
      <td>39.0</td>
      <td>6-6</td>
      <td>220.0</td>
      <td>North Carolina</td>
      <td>4088019.0</td>
    </tr>
    <tr>
      <th>363</th>
      <td>Victor Oladipo</td>
      <td>Orlando Magic</td>
      <td>5.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-4</td>
      <td>210.0</td>
      <td>Indiana</td>
      <td>5192520.0</td>
    </tr>
    <tr>
      <th>343</th>
      <td>Udonis Haslem</td>
      <td>Miami Heat</td>
      <td>40.0</td>
      <td>PF</td>
      <td>36.0</td>
      <td>6-8</td>
      <td>235.0</td>
      <td>Florida</td>
      <td>2854940.0</td>
    </tr>
    <tr>
      <th>401</th>
      <td>Tyus Jones</td>
      <td>Minnesota Timberwolves</td>
      <td>1.0</td>
      <td>PG</td>
      <td>20.0</td>
      <td>6-2</td>
      <td>195.0</td>
      <td>Duke</td>
      <td>1282080.0</td>
    </tr>
    <tr>
      <th>124</th>
      <td>Tyson Chandler</td>
      <td>Phoenix Suns</td>
      <td>4.0</td>
      <td>C</td>
      <td>33.0</td>
      <td>7-1</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>13000000.0</td>
    </tr>
    <tr>
      <th>285</th>
      <td>Tyreke Evans</td>
      <td>New Orleans Pelicans</td>
      <td>1.0</td>
      <td>SG</td>
      <td>26.0</td>
      <td>6-6</td>
      <td>220.0</td>
      <td>Memphis</td>
      <td>10734586.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Tyler Zeller</td>
      <td>Boston Celtics</td>
      <td>44.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>253.0</td>
      <td>North Carolina</td>
      <td>2616975.0</td>
    </tr>
    <tr>
      <th>345</th>
      <td>Tyler Johnson</td>
      <td>Miami Heat</td>
      <td>8.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-4</td>
      <td>186.0</td>
      <td>Fresno State</td>
      <td>845059.0</td>
    </tr>
    <tr>
      <th>327</th>
      <td>Tyler Hansbrough</td>
      <td>Charlotte Hornets</td>
      <td>50.0</td>
      <td>PF</td>
      <td>30.0</td>
      <td>6-9</td>
      <td>250.0</td>
      <td>North Carolina</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>215</th>
      <td>Tyler Ennis</td>
      <td>Milwaukee Bucks</td>
      <td>11.0</td>
      <td>PG</td>
      <td>21.0</td>
      <td>6-3</td>
      <td>194.0</td>
      <td>Syracuse</td>
      <td>1662360.0</td>
    </tr>
    <tr>
      <th>203</th>
      <td>Ty Lawson</td>
      <td>Indiana Pacers</td>
      <td>10.0</td>
      <td>PG</td>
      <td>28.0</td>
      <td>5-11</td>
      <td>195.0</td>
      <td>North Carolina</td>
      <td>211744.0</td>
    </tr>
    <tr>
      <th>325</th>
      <td>Troy Daniels</td>
      <td>Charlotte Hornets</td>
      <td>30.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-4</td>
      <td>205.0</td>
      <td>Virginia Commonwealth</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>179</th>
      <td>Tristan Thompson</td>
      <td>Cleveland Cavaliers</td>
      <td>13.0</td>
      <td>C</td>
      <td>25.0</td>
      <td>6-9</td>
      <td>238.0</td>
      <td>Texas</td>
      <td>14260870.0</td>
    </tr>
    <tr>
      <th>452</th>
      <td>Trey Lyles</td>
      <td>Utah Jazz</td>
      <td>41.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-10</td>
      <td>234.0</td>
      <td>Kentucky</td>
      <td>2239800.0</td>
    </tr>
    <tr>
      <th>443</th>
      <td>Trey Burke</td>
      <td>Utah Jazz</td>
      <td>3.0</td>
      <td>PG</td>
      <td>23.0</td>
      <td>6-1</td>
      <td>191.0</td>
      <td>Michigan</td>
      <td>2658240.0</td>
    </tr>
    <tr>
      <th>442</th>
      <td>Trevor Booker</td>
      <td>Utah Jazz</td>
      <td>33.0</td>
      <td>PF</td>
      <td>28.0</td>
      <td>6-8</td>
      <td>228.0</td>
      <td>Clemson</td>
      <td>4775000.0</td>
    </tr>
    <tr>
      <th>242</th>
      <td>Trevor Ariza</td>
      <td>Houston Rockets</td>
      <td>1.0</td>
      <td>SF</td>
      <td>30.0</td>
      <td>6-8</td>
      <td>215.0</td>
      <td>UCLA</td>
      <td>8193030.0</td>
    </tr>
    <tr>
      <th>45</th>
      <td>Tony Wroten</td>
      <td>New York Knicks</td>
      <td>5.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-6</td>
      <td>205.0</td>
      <td>Washington</td>
      <td>167406.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>421</th>
      <td>Anthony Morrow</td>
      <td>Oklahoma City Thunder</td>
      <td>2.0</td>
      <td>SG</td>
      <td>30.0</td>
      <td>6-5</td>
      <td>210.0</td>
      <td>Georgia Tech</td>
      <td>3344000.0</td>
    </tr>
    <tr>
      <th>281</th>
      <td>Anthony Davis</td>
      <td>New Orleans Pelicans</td>
      <td>23.0</td>
      <td>PF</td>
      <td>23.0</td>
      <td>6-10</td>
      <td>253.0</td>
      <td>Kentucky</td>
      <td>7070730.0</td>
    </tr>
    <tr>
      <th>108</th>
      <td>Anthony Brown</td>
      <td>Los Angeles Lakers</td>
      <td>3.0</td>
      <td>SF</td>
      <td>23.0</td>
      <td>6-7</td>
      <td>210.0</td>
      <td>Stanford</td>
      <td>700000.0</td>
    </tr>
    <tr>
      <th>411</th>
      <td>Andrew Wiggins</td>
      <td>Minnesota Timberwolves</td>
      <td>22.0</td>
      <td>SG</td>
      <td>21.0</td>
      <td>6-8</td>
      <td>199.0</td>
      <td>Kansas</td>
      <td>5758680.0</td>
    </tr>
    <tr>
      <th>362</th>
      <td>Andrew Nicholson</td>
      <td>Orlando Magic</td>
      <td>44.0</td>
      <td>PF</td>
      <td>26.0</td>
      <td>6-9</td>
      <td>250.0</td>
      <td>St. Bonaventure</td>
      <td>2380593.0</td>
    </tr>
    <tr>
      <th>248</th>
      <td>Andrew Goudelock</td>
      <td>Houston Rockets</td>
      <td>0.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-3</td>
      <td>200.0</td>
      <td>Charleston</td>
      <td>200600.0</td>
    </tr>
    <tr>
      <th>78</th>
      <td>Andrew Bogut</td>
      <td>Golden State Warriors</td>
      <td>12.0</td>
      <td>C</td>
      <td>31.0</td>
      <td>7-0</td>
      <td>260.0</td>
      <td>Utah</td>
      <td>13800000.0</td>
    </tr>
    <tr>
      <th>423</th>
      <td>Andre Roberson</td>
      <td>Oklahoma City Thunder</td>
      <td>21.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-7</td>
      <td>210.0</td>
      <td>Colorado</td>
      <td>1210800.0</td>
    </tr>
    <tr>
      <th>304</th>
      <td>Andre Miller</td>
      <td>San Antonio Spurs</td>
      <td>24.0</td>
      <td>PG</td>
      <td>40.0</td>
      <td>6-3</td>
      <td>200.0</td>
      <td>Utah</td>
      <td>250750.0</td>
    </tr>
    <tr>
      <th>83</th>
      <td>Andre Iguodala</td>
      <td>Golden State Warriors</td>
      <td>9.0</td>
      <td>SF</td>
      <td>32.0</td>
      <td>6-6</td>
      <td>215.0</td>
      <td>Arizona</td>
      <td>11710456.0</td>
    </tr>
    <tr>
      <th>188</th>
      <td>Andre Drummond</td>
      <td>Detroit Pistons</td>
      <td>0.0</td>
      <td>C</td>
      <td>22.0</td>
      <td>6-11</td>
      <td>279.0</td>
      <td>Connecticut</td>
      <td>3272091.0</td>
    </tr>
    <tr>
      <th>90</th>
      <td>Anderson Varejao</td>
      <td>Golden State Warriors</td>
      <td>18.0</td>
      <td>PF</td>
      <td>33.0</td>
      <td>6-11</td>
      <td>273.0</td>
      <td>NaN</td>
      <td>289755.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Amir Johnson</td>
      <td>Boston Celtics</td>
      <td>90.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>348</th>
      <td>Amar'e Stoudemire</td>
      <td>Miami Heat</td>
      <td>5.0</td>
      <td>PF</td>
      <td>33.0</td>
      <td>6-10</td>
      <td>245.0</td>
      <td>NaN</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>287</th>
      <td>Alonzo Gee</td>
      <td>New Orleans Pelicans</td>
      <td>15.0</td>
      <td>SF</td>
      <td>29.0</td>
      <td>6-6</td>
      <td>225.0</td>
      <td>Alabama</td>
      <td>1320000.0</td>
    </tr>
    <tr>
      <th>430</th>
      <td>Allen Crabbe</td>
      <td>Portland Trail Blazers</td>
      <td>23.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-6</td>
      <td>210.0</td>
      <td>California</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>275</th>
      <td>Alexis Ajinca</td>
      <td>New Orleans Pelicans</td>
      <td>42.0</td>
      <td>C</td>
      <td>28.0</td>
      <td>7-2</td>
      <td>248.0</td>
      <td>NaN</td>
      <td>4389607.0</td>
    </tr>
    <tr>
      <th>273</th>
      <td>Alex Stepheson</td>
      <td>Memphis Grizzlies</td>
      <td>35.0</td>
      <td>PF</td>
      <td>28.0</td>
      <td>6-10</td>
      <td>270.0</td>
      <td>USC</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>128</th>
      <td>Alex Len</td>
      <td>Phoenix Suns</td>
      <td>21.0</td>
      <td>C</td>
      <td>22.0</td>
      <td>7-1</td>
      <td>260.0</td>
      <td>Maryland</td>
      <td>3807120.0</td>
    </tr>
    <tr>
      <th>444</th>
      <td>Alec Burks</td>
      <td>Utah Jazz</td>
      <td>10.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-6</td>
      <td>214.0</td>
      <td>Colorado</td>
      <td>9463484.0</td>
    </tr>
    <tr>
      <th>135</th>
      <td>Alan Williams</td>
      <td>Phoenix Suns</td>
      <td>15.0</td>
      <td>C</td>
      <td>23.0</td>
      <td>6-8</td>
      <td>260.0</td>
      <td>UC Santa Barbara</td>
      <td>83397.0</td>
    </tr>
    <tr>
      <th>368</th>
      <td>Alan Anderson</td>
      <td>Washington Wizards</td>
      <td>6.0</td>
      <td>SG</td>
      <td>33.0</td>
      <td>6-6</td>
      <td>220.0</td>
      <td>Michigan State</td>
      <td>4000000.0</td>
    </tr>
    <tr>
      <th>428</th>
      <td>Al-Farouq Aminu</td>
      <td>Portland Trail Blazers</td>
      <td>8.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-9</td>
      <td>215.0</td>
      <td>Wake Forest</td>
      <td>8042895.0</td>
    </tr>
    <tr>
      <th>330</th>
      <td>Al Jefferson</td>
      <td>Charlotte Hornets</td>
      <td>25.0</td>
      <td>C</td>
      <td>31.0</td>
      <td>6-10</td>
      <td>289.0</td>
      <td>NaN</td>
      <td>13500000.0</td>
    </tr>
    <tr>
      <th>312</th>
      <td>Al Horford</td>
      <td>Atlanta Hawks</td>
      <td>15.0</td>
      <td>C</td>
      <td>30.0</td>
      <td>6-10</td>
      <td>245.0</td>
      <td>Florida</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>404</th>
      <td>Adreian Payne</td>
      <td>Minnesota Timberwolves</td>
      <td>33.0</td>
      <td>PF</td>
      <td>25.0</td>
      <td>6-10</td>
      <td>237.0</td>
      <td>Michigan State</td>
      <td>1938840.0</td>
    </tr>
    <tr>
      <th>328</th>
      <td>Aaron Harrison</td>
      <td>Charlotte Hornets</td>
      <td>9.0</td>
      <td>SG</td>
      <td>21.0</td>
      <td>6-6</td>
      <td>210.0</td>
      <td>Kentucky</td>
      <td>525093.0</td>
    </tr>
    <tr>
      <th>356</th>
      <td>Aaron Gordon</td>
      <td>Orlando Magic</td>
      <td>0.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-9</td>
      <td>220.0</td>
      <td>Arizona</td>
      <td>4171680.0</td>
    </tr>
    <tr>
      <th>152</th>
      <td>Aaron Brooks</td>
      <td>Chicago Bulls</td>
      <td>0.0</td>
      <td>PG</td>
      <td>31.0</td>
      <td>6-0</td>
      <td>161.0</td>
      <td>Oregon</td>
      <td>2250000.0</td>
    </tr>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>458 rows × 9 columns</p>
</div>




```python
nba.sort_values("Age", ascending = False)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>304</th>
      <td>Andre Miller</td>
      <td>San Antonio Spurs</td>
      <td>24.0</td>
      <td>PG</td>
      <td>40.0</td>
      <td>6-3</td>
      <td>200.0</td>
      <td>Utah</td>
      <td>250750.0</td>
    </tr>
    <tr>
      <th>400</th>
      <td>Kevin Garnett</td>
      <td>Minnesota Timberwolves</td>
      <td>21.0</td>
      <td>PF</td>
      <td>40.0</td>
      <td>6-11</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>8500000.0</td>
    </tr>
    <tr>
      <th>298</th>
      <td>Tim Duncan</td>
      <td>San Antonio Spurs</td>
      <td>21.0</td>
      <td>C</td>
      <td>40.0</td>
      <td>6-11</td>
      <td>250.0</td>
      <td>Wake Forest</td>
      <td>5250000.0</td>
    </tr>
    <tr>
      <th>261</th>
      <td>Vince Carter</td>
      <td>Memphis Grizzlies</td>
      <td>15.0</td>
      <td>SG</td>
      <td>39.0</td>
      <td>6-6</td>
      <td>220.0</td>
      <td>North Carolina</td>
      <td>4088019.0</td>
    </tr>
    <tr>
      <th>102</th>
      <td>Pablo Prigioni</td>
      <td>Los Angeles Clippers</td>
      <td>9.0</td>
      <td>PG</td>
      <td>39.0</td>
      <td>6-3</td>
      <td>185.0</td>
      <td>NaN</td>
      <td>947726.0</td>
    </tr>
    <tr>
      <th>299</th>
      <td>Manu Ginobili</td>
      <td>San Antonio Spurs</td>
      <td>20.0</td>
      <td>SG</td>
      <td>38.0</td>
      <td>6-6</td>
      <td>205.0</td>
      <td>NaN</td>
      <td>2814000.0</td>
    </tr>
    <tr>
      <th>101</th>
      <td>Paul Pierce</td>
      <td>Los Angeles Clippers</td>
      <td>34.0</td>
      <td>SF</td>
      <td>38.0</td>
      <td>6-7</td>
      <td>235.0</td>
      <td>Kansas</td>
      <td>3376000.0</td>
    </tr>
    <tr>
      <th>256</th>
      <td>Jason Terry</td>
      <td>Houston Rockets</td>
      <td>31.0</td>
      <td>SG</td>
      <td>38.0</td>
      <td>6-2</td>
      <td>185.0</td>
      <td>Arizona</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>420</th>
      <td>Nazr Mohammed</td>
      <td>Oklahoma City Thunder</td>
      <td>13.0</td>
      <td>C</td>
      <td>38.0</td>
      <td>6-10</td>
      <td>250.0</td>
      <td>Kentucky</td>
      <td>222888.0</td>
    </tr>
    <tr>
      <th>236</th>
      <td>Dirk Nowitzki</td>
      <td>Dallas Mavericks</td>
      <td>41.0</td>
      <td>PF</td>
      <td>37.0</td>
      <td>7-0</td>
      <td>245.0</td>
      <td>NaN</td>
      <td>8333334.0</td>
    </tr>
    <tr>
      <th>46</th>
      <td>Elton Brand</td>
      <td>Philadelphia 76ers</td>
      <td>42.0</td>
      <td>PF</td>
      <td>37.0</td>
      <td>6-9</td>
      <td>254.0</td>
      <td>Duke</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>259</th>
      <td>Chris Andersen</td>
      <td>Memphis Grizzlies</td>
      <td>7.0</td>
      <td>PF</td>
      <td>37.0</td>
      <td>6-10</td>
      <td>245.0</td>
      <td>Blinn College</td>
      <td>5000000.0</td>
    </tr>
    <tr>
      <th>109</th>
      <td>Kobe Bryant</td>
      <td>Los Angeles Lakers</td>
      <td>24.0</td>
      <td>SF</td>
      <td>37.0</td>
      <td>6-6</td>
      <td>212.0</td>
      <td>NaN</td>
      <td>25000000.0</td>
    </tr>
    <tr>
      <th>406</th>
      <td>Tayshaun Prince</td>
      <td>Minnesota Timberwolves</td>
      <td>12.0</td>
      <td>SF</td>
      <td>36.0</td>
      <td>6-9</td>
      <td>212.0</td>
      <td>Kentucky</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>72</th>
      <td>Luis Scola</td>
      <td>Toronto Raptors</td>
      <td>4.0</td>
      <td>PF</td>
      <td>36.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>2900000.0</td>
    </tr>
    <tr>
      <th>139</th>
      <td>Caron Butler</td>
      <td>Sacramento Kings</td>
      <td>31.0</td>
      <td>SF</td>
      <td>36.0</td>
      <td>6-7</td>
      <td>228.0</td>
      <td>Connecticut</td>
      <td>1449187.0</td>
    </tr>
    <tr>
      <th>296</th>
      <td>Matt Bonner</td>
      <td>San Antonio Spurs</td>
      <td>15.0</td>
      <td>C</td>
      <td>36.0</td>
      <td>6-10</td>
      <td>235.0</td>
      <td>Florida</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>119</th>
      <td>Metta World Peace</td>
      <td>Los Angeles Lakers</td>
      <td>37.0</td>
      <td>SF</td>
      <td>36.0</td>
      <td>6-7</td>
      <td>260.0</td>
      <td>St. John's</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>392</th>
      <td>Mike Miller</td>
      <td>Denver Nuggets</td>
      <td>3.0</td>
      <td>SG</td>
      <td>36.0</td>
      <td>6-8</td>
      <td>218.0</td>
      <td>Florida</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>183</th>
      <td>Steve Blake</td>
      <td>Detroit Pistons</td>
      <td>22.0</td>
      <td>PG</td>
      <td>36.0</td>
      <td>6-3</td>
      <td>172.0</td>
      <td>Maryland</td>
      <td>2170465.0</td>
    </tr>
    <tr>
      <th>343</th>
      <td>Udonis Haslem</td>
      <td>Miami Heat</td>
      <td>40.0</td>
      <td>PF</td>
      <td>36.0</td>
      <td>6-8</td>
      <td>235.0</td>
      <td>Florida</td>
      <td>2854940.0</td>
    </tr>
    <tr>
      <th>93</th>
      <td>Jamal Crawford</td>
      <td>Los Angeles Clippers</td>
      <td>11.0</td>
      <td>SG</td>
      <td>36.0</td>
      <td>6-5</td>
      <td>195.0</td>
      <td>Michigan</td>
      <td>5675000.0</td>
    </tr>
    <tr>
      <th>260</th>
      <td>Matt Barnes</td>
      <td>Memphis Grizzlies</td>
      <td>22.0</td>
      <td>SF</td>
      <td>36.0</td>
      <td>6-7</td>
      <td>226.0</td>
      <td>UCLA</td>
      <td>3542500.0</td>
    </tr>
    <tr>
      <th>413</th>
      <td>Nick Collison</td>
      <td>Oklahoma City Thunder</td>
      <td>4.0</td>
      <td>PF</td>
      <td>35.0</td>
      <td>6-10</td>
      <td>255.0</td>
      <td>Kansas</td>
      <td>3750000.0</td>
    </tr>
    <tr>
      <th>314</th>
      <td>Kyle Korver</td>
      <td>Atlanta Hawks</td>
      <td>26.0</td>
      <td>SG</td>
      <td>35.0</td>
      <td>6-7</td>
      <td>212.0</td>
      <td>Creighton</td>
      <td>5746479.0</td>
    </tr>
    <tr>
      <th>156</th>
      <td>Pau Gasol</td>
      <td>Chicago Bulls</td>
      <td>16.0</td>
      <td>C</td>
      <td>35.0</td>
      <td>7-0</td>
      <td>250.0</td>
      <td>NaN</td>
      <td>7448760.0</td>
    </tr>
    <tr>
      <th>308</th>
      <td>David West</td>
      <td>San Antonio Spurs</td>
      <td>30.0</td>
      <td>PF</td>
      <td>35.0</td>
      <td>6-9</td>
      <td>250.0</td>
      <td>Xavier</td>
      <td>1499187.0</td>
    </tr>
    <tr>
      <th>311</th>
      <td>Kirk Hinrich</td>
      <td>Atlanta Hawks</td>
      <td>12.0</td>
      <td>SG</td>
      <td>35.0</td>
      <td>6-4</td>
      <td>190.0</td>
      <td>Kansas</td>
      <td>2854940.0</td>
    </tr>
    <tr>
      <th>154</th>
      <td>Mike Dunleavy</td>
      <td>Chicago Bulls</td>
      <td>34.0</td>
      <td>SG</td>
      <td>35.0</td>
      <td>6-9</td>
      <td>230.0</td>
      <td>Duke</td>
      <td>4500000.0</td>
    </tr>
    <tr>
      <th>172</th>
      <td>James Jones</td>
      <td>Cleveland Cavaliers</td>
      <td>1.0</td>
      <td>SG</td>
      <td>35.0</td>
      <td>6-8</td>
      <td>218.0</td>
      <td>Miami (FL)</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>215</th>
      <td>Tyler Ennis</td>
      <td>Milwaukee Bucks</td>
      <td>11.0</td>
      <td>PG</td>
      <td>21.0</td>
      <td>6-3</td>
      <td>194.0</td>
      <td>Syracuse</td>
      <td>1662360.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Jordan Mickey</td>
      <td>Boston Celtics</td>
      <td>55.0</td>
      <td>PF</td>
      <td>21.0</td>
      <td>6-8</td>
      <td>235.0</td>
      <td>LSU</td>
      <td>1170960.0</td>
    </tr>
    <tr>
      <th>411</th>
      <td>Andrew Wiggins</td>
      <td>Minnesota Timberwolves</td>
      <td>22.0</td>
      <td>SG</td>
      <td>21.0</td>
      <td>6-8</td>
      <td>199.0</td>
      <td>Kansas</td>
      <td>5758680.0</td>
    </tr>
    <tr>
      <th>357</th>
      <td>Mario Hezonja</td>
      <td>Orlando Magic</td>
      <td>23.0</td>
      <td>SG</td>
      <td>21.0</td>
      <td>6-8</td>
      <td>218.0</td>
      <td>NaN</td>
      <td>3741480.0</td>
    </tr>
    <tr>
      <th>390</th>
      <td>Nikola Jokic</td>
      <td>Denver Nuggets</td>
      <td>15.0</td>
      <td>C</td>
      <td>21.0</td>
      <td>6-10</td>
      <td>250.0</td>
      <td>NaN</td>
      <td>1300000.0</td>
    </tr>
    <tr>
      <th>389</th>
      <td>Gary Harris</td>
      <td>Denver Nuggets</td>
      <td>14.0</td>
      <td>SG</td>
      <td>21.0</td>
      <td>6-4</td>
      <td>210.0</td>
      <td>Michigan State</td>
      <td>1584480.0</td>
    </tr>
    <tr>
      <th>211</th>
      <td>Giannis Antetokounmpo</td>
      <td>Milwaukee Bucks</td>
      <td>34.0</td>
      <td>SF</td>
      <td>21.0</td>
      <td>6-11</td>
      <td>222.0</td>
      <td>NaN</td>
      <td>1953960.0</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Chris McCullough</td>
      <td>Brooklyn Nets</td>
      <td>1.0</td>
      <td>PF</td>
      <td>21.0</td>
      <td>6-11</td>
      <td>200.0</td>
      <td>Syracuse</td>
      <td>1140240.0</td>
    </tr>
    <tr>
      <th>452</th>
      <td>Trey Lyles</td>
      <td>Utah Jazz</td>
      <td>41.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-10</td>
      <td>234.0</td>
      <td>Kentucky</td>
      <td>2239800.0</td>
    </tr>
    <tr>
      <th>116</th>
      <td>D'Angelo Russell</td>
      <td>Los Angeles Lakers</td>
      <td>1.0</td>
      <td>PG</td>
      <td>20.0</td>
      <td>6-5</td>
      <td>195.0</td>
      <td>Ohio State</td>
      <td>5103120.0</td>
    </tr>
    <tr>
      <th>208</th>
      <td>Myles Turner</td>
      <td>Indiana Pacers</td>
      <td>33.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-11</td>
      <td>243.0</td>
      <td>Texas</td>
      <td>2357760.0</td>
    </tr>
    <tr>
      <th>352</th>
      <td>Justise Winslow</td>
      <td>Miami Heat</td>
      <td>20.0</td>
      <td>SF</td>
      <td>20.0</td>
      <td>6-7</td>
      <td>225.0</td>
      <td>Duke</td>
      <td>2481720.0</td>
    </tr>
    <tr>
      <th>85</th>
      <td>Kevon Looney</td>
      <td>Golden State Warriors</td>
      <td>36.0</td>
      <td>SF</td>
      <td>20.0</td>
      <td>6-9</td>
      <td>220.0</td>
      <td>UCLA</td>
      <td>1131960.0</td>
    </tr>
    <tr>
      <th>445</th>
      <td>Dante Exum</td>
      <td>Utah Jazz</td>
      <td>11.0</td>
      <td>PG</td>
      <td>20.0</td>
      <td>6-6</td>
      <td>190.0</td>
      <td>NaN</td>
      <td>3777720.0</td>
    </tr>
    <tr>
      <th>356</th>
      <td>Aaron Gordon</td>
      <td>Orlando Magic</td>
      <td>0.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-9</td>
      <td>220.0</td>
      <td>Arizona</td>
      <td>4171680.0</td>
    </tr>
    <tr>
      <th>62</th>
      <td>Bruno Caboclo</td>
      <td>Toronto Raptors</td>
      <td>20.0</td>
      <td>SF</td>
      <td>20.0</td>
      <td>6-9</td>
      <td>205.0</td>
      <td>NaN</td>
      <td>1524000.0</td>
    </tr>
    <tr>
      <th>441</th>
      <td>Noah Vonleh</td>
      <td>Portland Trail Blazers</td>
      <td>21.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>Indiana</td>
      <td>2637720.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>James Young</td>
      <td>Boston Celtics</td>
      <td>13.0</td>
      <td>SG</td>
      <td>20.0</td>
      <td>6-6</td>
      <td>215.0</td>
      <td>Kentucky</td>
      <td>1749840.0</td>
    </tr>
    <tr>
      <th>192</th>
      <td>Stanley Johnson</td>
      <td>Detroit Pistons</td>
      <td>3.0</td>
      <td>SF</td>
      <td>20.0</td>
      <td>6-7</td>
      <td>245.0</td>
      <td>Arizona</td>
      <td>2841960.0</td>
    </tr>
    <tr>
      <th>427</th>
      <td>Cliff Alexander</td>
      <td>Portland Trail Blazers</td>
      <td>34.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-8</td>
      <td>240.0</td>
      <td>Kansas</td>
      <td>525093.0</td>
    </tr>
    <tr>
      <th>377</th>
      <td>Kelly Oubre Jr.</td>
      <td>Washington Wizards</td>
      <td>12.0</td>
      <td>SF</td>
      <td>20.0</td>
      <td>6-7</td>
      <td>205.0</td>
      <td>Kansas</td>
      <td>1920240.0</td>
    </tr>
    <tr>
      <th>56</th>
      <td>Jahlil Okafor</td>
      <td>Philadelphia 76ers</td>
      <td>8.0</td>
      <td>C</td>
      <td>20.0</td>
      <td>6-11</td>
      <td>275.0</td>
      <td>Duke</td>
      <td>4582680.0</td>
    </tr>
    <tr>
      <th>393</th>
      <td>Emmanuel Mudiay</td>
      <td>Denver Nuggets</td>
      <td>0.0</td>
      <td>PG</td>
      <td>20.0</td>
      <td>6-5</td>
      <td>200.0</td>
      <td>NaN</td>
      <td>3102240.0</td>
    </tr>
    <tr>
      <th>410</th>
      <td>Karl-Anthony Towns</td>
      <td>Minnesota Timberwolves</td>
      <td>32.0</td>
      <td>C</td>
      <td>20.0</td>
      <td>7-0</td>
      <td>244.0</td>
      <td>Kentucky</td>
      <td>5703600.0</td>
    </tr>
    <tr>
      <th>40</th>
      <td>Kristaps Porzingis</td>
      <td>New York Knicks</td>
      <td>6.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>7-3</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>4131720.0</td>
    </tr>
    <tr>
      <th>401</th>
      <td>Tyus Jones</td>
      <td>Minnesota Timberwolves</td>
      <td>1.0</td>
      <td>PG</td>
      <td>20.0</td>
      <td>6-2</td>
      <td>195.0</td>
      <td>Duke</td>
      <td>1282080.0</td>
    </tr>
    <tr>
      <th>60</th>
      <td>Christian Wood</td>
      <td>Philadelphia 76ers</td>
      <td>35.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-11</td>
      <td>220.0</td>
      <td>UNLV</td>
      <td>525093.0</td>
    </tr>
    <tr>
      <th>226</th>
      <td>Rashad Vaughn</td>
      <td>Milwaukee Bucks</td>
      <td>20.0</td>
      <td>SG</td>
      <td>19.0</td>
      <td>6-6</td>
      <td>202.0</td>
      <td>UNLV</td>
      <td>1733040.0</td>
    </tr>
    <tr>
      <th>122</th>
      <td>Devin Booker</td>
      <td>Phoenix Suns</td>
      <td>1.0</td>
      <td>SG</td>
      <td>19.0</td>
      <td>6-6</td>
      <td>206.0</td>
      <td>Kentucky</td>
      <td>2127840.0</td>
    </tr>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>458 rows × 9 columns</p>
</div>




```python
# Finding the 3 highest salary in NBA
nba.sort_values("Salary", ascending = False).head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>109</th>
      <td>Kobe Bryant</td>
      <td>Los Angeles Lakers</td>
      <td>24.0</td>
      <td>SF</td>
      <td>37.0</td>
      <td>6-6</td>
      <td>212.0</td>
      <td>NaN</td>
      <td>25000000.0</td>
    </tr>
    <tr>
      <th>169</th>
      <td>LeBron James</td>
      <td>Cleveland Cavaliers</td>
      <td>23.0</td>
      <td>SF</td>
      <td>31.0</td>
      <td>6-8</td>
      <td>250.0</td>
      <td>NaN</td>
      <td>22970500.0</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Carmelo Anthony</td>
      <td>New York Knicks</td>
      <td>7.0</td>
      <td>SF</td>
      <td>32.0</td>
      <td>6-8</td>
      <td>240.0</td>
      <td>Syracuse</td>
      <td>22875000.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.sort_values("Salary").tail()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>350</th>
      <td>Briante Weber</td>
      <td>Miami Heat</td>
      <td>12.0</td>
      <td>PG</td>
      <td>23.0</td>
      <td>6-2</td>
      <td>165.0</td>
      <td>Virginia Commonwealth</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>353</th>
      <td>Dorell Wright</td>
      <td>Miami Heat</td>
      <td>11.0</td>
      <td>SF</td>
      <td>30.0</td>
      <td>6-9</td>
      <td>205.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>397</th>
      <td>Axel Toupane</td>
      <td>Denver Nuggets</td>
      <td>6.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-7</td>
      <td>210.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>409</th>
      <td>Greg Smith</td>
      <td>Minnesota Timberwolves</td>
      <td>4.0</td>
      <td>PF</td>
      <td>25.0</td>
      <td>6-10</td>
      <td>250.0</td>
      <td>Fresno State</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.sort_values("Salary", na_position = "first")
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>46</th>
      <td>Elton Brand</td>
      <td>Philadelphia 76ers</td>
      <td>42.0</td>
      <td>PF</td>
      <td>37.0</td>
      <td>6-9</td>
      <td>254.0</td>
      <td>Duke</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>171</th>
      <td>Dahntay Jones</td>
      <td>Cleveland Cavaliers</td>
      <td>30.0</td>
      <td>SG</td>
      <td>35.0</td>
      <td>6-6</td>
      <td>225.0</td>
      <td>Duke</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>264</th>
      <td>Jordan Farmar</td>
      <td>Memphis Grizzlies</td>
      <td>4.0</td>
      <td>PG</td>
      <td>29.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>UCLA</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>269</th>
      <td>Ray McCallum</td>
      <td>Memphis Grizzlies</td>
      <td>5.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-3</td>
      <td>190.0</td>
      <td>Detroit</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>270</th>
      <td>Xavier Munford</td>
      <td>Memphis Grizzlies</td>
      <td>14.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-3</td>
      <td>180.0</td>
      <td>Rhode Island</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>273</th>
      <td>Alex Stepheson</td>
      <td>Memphis Grizzlies</td>
      <td>35.0</td>
      <td>PF</td>
      <td>28.0</td>
      <td>6-10</td>
      <td>270.0</td>
      <td>USC</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>350</th>
      <td>Briante Weber</td>
      <td>Miami Heat</td>
      <td>12.0</td>
      <td>PG</td>
      <td>23.0</td>
      <td>6-2</td>
      <td>165.0</td>
      <td>Virginia Commonwealth</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>353</th>
      <td>Dorell Wright</td>
      <td>Miami Heat</td>
      <td>11.0</td>
      <td>SF</td>
      <td>30.0</td>
      <td>6-9</td>
      <td>205.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>397</th>
      <td>Axel Toupane</td>
      <td>Denver Nuggets</td>
      <td>6.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-7</td>
      <td>210.0</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>409</th>
      <td>Greg Smith</td>
      <td>Minnesota Timberwolves</td>
      <td>4.0</td>
      <td>PF</td>
      <td>25.0</td>
      <td>6-10</td>
      <td>250.0</td>
      <td>Fresno State</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Thanasis Antetokounmpo</td>
      <td>New York Knicks</td>
      <td>43.0</td>
      <td>SF</td>
      <td>23.0</td>
      <td>6-7</td>
      <td>205.0</td>
      <td>NaN</td>
      <td>30888.0</td>
    </tr>
    <tr>
      <th>291</th>
      <td>Orlando Johnson</td>
      <td>New Orleans Pelicans</td>
      <td>0.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>220.0</td>
      <td>UC Santa Barbara</td>
      <td>55722.0</td>
    </tr>
    <tr>
      <th>130</th>
      <td>Phil Pressey</td>
      <td>Phoenix Suns</td>
      <td>25.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>5-11</td>
      <td>175.0</td>
      <td>Missouri</td>
      <td>55722.0</td>
    </tr>
    <tr>
      <th>135</th>
      <td>Alan Williams</td>
      <td>Phoenix Suns</td>
      <td>15.0</td>
      <td>C</td>
      <td>23.0</td>
      <td>6-8</td>
      <td>260.0</td>
      <td>UC Santa Barbara</td>
      <td>83397.0</td>
    </tr>
    <tr>
      <th>175</th>
      <td>Jordan McRae</td>
      <td>Cleveland Cavaliers</td>
      <td>12.0</td>
      <td>SG</td>
      <td>25.0</td>
      <td>6-5</td>
      <td>179.0</td>
      <td>Tennessee</td>
      <td>111196.0</td>
    </tr>
    <tr>
      <th>92</th>
      <td>Jeff Ayres</td>
      <td>Los Angeles Clippers</td>
      <td>19.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-9</td>
      <td>250.0</td>
      <td>Arizona State</td>
      <td>111444.0</td>
    </tr>
    <tr>
      <th>184</th>
      <td>Lorenzo Brown</td>
      <td>Detroit Pistons</td>
      <td>17.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-5</td>
      <td>189.0</td>
      <td>North Carolina State</td>
      <td>111444.0</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Sean Kilpatrick</td>
      <td>Brooklyn Nets</td>
      <td>6.0</td>
      <td>SG</td>
      <td>26.0</td>
      <td>6-4</td>
      <td>219.0</td>
      <td>Cincinnati</td>
      <td>134215.0</td>
    </tr>
    <tr>
      <th>45</th>
      <td>Tony Wroten</td>
      <td>New York Knicks</td>
      <td>5.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-6</td>
      <td>205.0</td>
      <td>Washington</td>
      <td>167406.0</td>
    </tr>
    <tr>
      <th>282</th>
      <td>Bryce Dejean-Jones</td>
      <td>New Orleans Pelicans</td>
      <td>31.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-6</td>
      <td>203.0</td>
      <td>Iowa State</td>
      <td>169883.0</td>
    </tr>
    <tr>
      <th>326</th>
      <td>Jorge Gutierrez</td>
      <td>Charlotte Hornets</td>
      <td>12.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-3</td>
      <td>189.0</td>
      <td>California</td>
      <td>189455.0</td>
    </tr>
    <tr>
      <th>381</th>
      <td>Marcus Thornton</td>
      <td>Washington Wizards</td>
      <td>15.0</td>
      <td>SF</td>
      <td>29.0</td>
      <td>6-4</td>
      <td>205.0</td>
      <td>LSU</td>
      <td>200600.0</td>
    </tr>
    <tr>
      <th>248</th>
      <td>Andrew Goudelock</td>
      <td>Houston Rockets</td>
      <td>0.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-3</td>
      <td>200.0</td>
      <td>Charleston</td>
      <td>200600.0</td>
    </tr>
    <tr>
      <th>303</th>
      <td>Kevin Martin</td>
      <td>San Antonio Spurs</td>
      <td>23.0</td>
      <td>SG</td>
      <td>33.0</td>
      <td>6-7</td>
      <td>199.0</td>
      <td>Western Carolina</td>
      <td>200600.0</td>
    </tr>
    <tr>
      <th>123</th>
      <td>Chase Budinger</td>
      <td>Phoenix Suns</td>
      <td>10.0</td>
      <td>SF</td>
      <td>28.0</td>
      <td>6-7</td>
      <td>209.0</td>
      <td>Arizona</td>
      <td>206192.0</td>
    </tr>
    <tr>
      <th>203</th>
      <td>Ty Lawson</td>
      <td>Indiana Pacers</td>
      <td>10.0</td>
      <td>PG</td>
      <td>28.0</td>
      <td>5-11</td>
      <td>195.0</td>
      <td>North Carolina</td>
      <td>211744.0</td>
    </tr>
    <tr>
      <th>420</th>
      <td>Nazr Mohammed</td>
      <td>Oklahoma City Thunder</td>
      <td>13.0</td>
      <td>C</td>
      <td>38.0</td>
      <td>6-10</td>
      <td>250.0</td>
      <td>Kentucky</td>
      <td>222888.0</td>
    </tr>
    <tr>
      <th>73</th>
      <td>Jason Thompson</td>
      <td>Toronto Raptors</td>
      <td>1.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-11</td>
      <td>250.0</td>
      <td>Rider</td>
      <td>245177.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>288</th>
      <td>Eric Gordon</td>
      <td>New Orleans Pelicans</td>
      <td>10.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-4</td>
      <td>215.0</td>
      <td>Indiana</td>
      <td>15514031.0</td>
    </tr>
    <tr>
      <th>111</th>
      <td>Roy Hibbert</td>
      <td>Los Angeles Lakers</td>
      <td>17.0</td>
      <td>C</td>
      <td>29.0</td>
      <td>7-2</td>
      <td>270.0</td>
      <td>Georgetown</td>
      <td>15592217.0</td>
    </tr>
    <tr>
      <th>249</th>
      <td>James Harden</td>
      <td>Houston Rockets</td>
      <td>13.0</td>
      <td>SG</td>
      <td>26.0</td>
      <td>6-5</td>
      <td>220.0</td>
      <td>Arizona State</td>
      <td>15756438.0</td>
    </tr>
    <tr>
      <th>382</th>
      <td>John Wall</td>
      <td>Washington Wizards</td>
      <td>2.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-4</td>
      <td>195.0</td>
      <td>Kentucky</td>
      <td>15851950.0</td>
    </tr>
    <tr>
      <th>143</th>
      <td>DeMarcus Cousins</td>
      <td>Sacramento Kings</td>
      <td>15.0</td>
      <td>C</td>
      <td>25.0</td>
      <td>6-11</td>
      <td>270.0</td>
      <td>Kentucky</td>
      <td>15851950.0</td>
    </tr>
    <tr>
      <th>189</th>
      <td>Tobias Harris</td>
      <td>Detroit Pistons</td>
      <td>34.0</td>
      <td>SF</td>
      <td>23.0</td>
      <td>6-9</td>
      <td>235.0</td>
      <td>Tennessee</td>
      <td>16000000.0</td>
    </tr>
    <tr>
      <th>153</th>
      <td>Jimmy Butler</td>
      <td>Chicago Bulls</td>
      <td>21.0</td>
      <td>SG</td>
      <td>26.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>Marquette</td>
      <td>16407500.0</td>
    </tr>
    <tr>
      <th>220</th>
      <td>Greg Monroe</td>
      <td>Milwaukee Bucks</td>
      <td>15.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>6-11</td>
      <td>265.0</td>
      <td>Georgetown</td>
      <td>16407500.0</td>
    </tr>
    <tr>
      <th>233</th>
      <td>Wesley Matthews</td>
      <td>Dallas Mavericks</td>
      <td>23.0</td>
      <td>SG</td>
      <td>29.0</td>
      <td>6-5</td>
      <td>220.0</td>
      <td>Marquette</td>
      <td>16407500.0</td>
    </tr>
    <tr>
      <th>301</th>
      <td>Kawhi Leonard</td>
      <td>San Antonio Spurs</td>
      <td>2.0</td>
      <td>SF</td>
      <td>24.0</td>
      <td>6-7</td>
      <td>230.0</td>
      <td>San Diego State</td>
      <td>16407500.0</td>
    </tr>
    <tr>
      <th>418</th>
      <td>Enes Kanter</td>
      <td>Oklahoma City Thunder</td>
      <td>11.0</td>
      <td>C</td>
      <td>24.0</td>
      <td>6-11</td>
      <td>245.0</td>
      <td>Kentucky</td>
      <td>16407500.0</td>
    </tr>
    <tr>
      <th>168</th>
      <td>Kyrie Irving</td>
      <td>Cleveland Cavaliers</td>
      <td>2.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-3</td>
      <td>193.0</td>
      <td>Duke</td>
      <td>16407501.0</td>
    </tr>
    <tr>
      <th>426</th>
      <td>Russell Westbrook</td>
      <td>Oklahoma City Thunder</td>
      <td>0.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-3</td>
      <td>200.0</td>
      <td>UCLA</td>
      <td>16744218.0</td>
    </tr>
    <tr>
      <th>199</th>
      <td>Paul George</td>
      <td>Indiana Pacers</td>
      <td>13.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-9</td>
      <td>220.0</td>
      <td>Fresno State</td>
      <td>17120106.0</td>
    </tr>
    <tr>
      <th>315</th>
      <td>Paul Millsap</td>
      <td>Atlanta Hawks</td>
      <td>4.0</td>
      <td>PF</td>
      <td>31.0</td>
      <td>6-8</td>
      <td>246.0</td>
      <td>Louisiana Tech</td>
      <td>18671659.0</td>
    </tr>
    <tr>
      <th>96</th>
      <td>Blake Griffin</td>
      <td>Los Angeles Clippers</td>
      <td>32.0</td>
      <td>PF</td>
      <td>27.0</td>
      <td>6-10</td>
      <td>251.0</td>
      <td>Oklahoma</td>
      <td>18907726.0</td>
    </tr>
    <tr>
      <th>265</th>
      <td>Marc Gasol</td>
      <td>Memphis Grizzlies</td>
      <td>33.0</td>
      <td>C</td>
      <td>31.0</td>
      <td>7-1</td>
      <td>255.0</td>
      <td>NaN</td>
      <td>19688000.0</td>
    </tr>
    <tr>
      <th>294</th>
      <td>LaMarcus Aldridge</td>
      <td>San Antonio Spurs</td>
      <td>12.0</td>
      <td>PF</td>
      <td>30.0</td>
      <td>6-11</td>
      <td>240.0</td>
      <td>Texas</td>
      <td>19689000.0</td>
    </tr>
    <tr>
      <th>174</th>
      <td>Kevin Love</td>
      <td>Cleveland Cavaliers</td>
      <td>0.0</td>
      <td>PF</td>
      <td>27.0</td>
      <td>6-10</td>
      <td>251.0</td>
      <td>UCLA</td>
      <td>19689000.0</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Brook Lopez</td>
      <td>Brooklyn Nets</td>
      <td>11.0</td>
      <td>C</td>
      <td>28.0</td>
      <td>7-0</td>
      <td>275.0</td>
      <td>Stanford</td>
      <td>19689000.0</td>
    </tr>
    <tr>
      <th>98</th>
      <td>DeAndre Jordan</td>
      <td>Los Angeles Clippers</td>
      <td>6.0</td>
      <td>C</td>
      <td>27.0</td>
      <td>6-11</td>
      <td>265.0</td>
      <td>Texas A&amp;M</td>
      <td>19689000.0</td>
    </tr>
    <tr>
      <th>349</th>
      <td>Dwyane Wade</td>
      <td>Miami Heat</td>
      <td>3.0</td>
      <td>SG</td>
      <td>34.0</td>
      <td>6-4</td>
      <td>220.0</td>
      <td>Marquette</td>
      <td>20000000.0</td>
    </tr>
    <tr>
      <th>164</th>
      <td>Derrick Rose</td>
      <td>Chicago Bulls</td>
      <td>1.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-3</td>
      <td>190.0</td>
      <td>Memphis</td>
      <td>20093064.0</td>
    </tr>
    <tr>
      <th>414</th>
      <td>Kevin Durant</td>
      <td>Oklahoma City Thunder</td>
      <td>35.0</td>
      <td>SF</td>
      <td>27.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>Texas</td>
      <td>20158622.0</td>
    </tr>
    <tr>
      <th>100</th>
      <td>Chris Paul</td>
      <td>Los Angeles Clippers</td>
      <td>3.0</td>
      <td>PG</td>
      <td>31.0</td>
      <td>6-0</td>
      <td>175.0</td>
      <td>Wake Forest</td>
      <td>21468695.0</td>
    </tr>
    <tr>
      <th>339</th>
      <td>Chris Bosh</td>
      <td>Miami Heat</td>
      <td>1.0</td>
      <td>PF</td>
      <td>32.0</td>
      <td>6-11</td>
      <td>235.0</td>
      <td>Georgia Tech</td>
      <td>22192730.0</td>
    </tr>
    <tr>
      <th>251</th>
      <td>Dwight Howard</td>
      <td>Houston Rockets</td>
      <td>12.0</td>
      <td>C</td>
      <td>30.0</td>
      <td>6-11</td>
      <td>265.0</td>
      <td>NaN</td>
      <td>22359364.0</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Carmelo Anthony</td>
      <td>New York Knicks</td>
      <td>7.0</td>
      <td>SF</td>
      <td>32.0</td>
      <td>6-8</td>
      <td>240.0</td>
      <td>Syracuse</td>
      <td>22875000.0</td>
    </tr>
    <tr>
      <th>169</th>
      <td>LeBron James</td>
      <td>Cleveland Cavaliers</td>
      <td>23.0</td>
      <td>SF</td>
      <td>31.0</td>
      <td>6-8</td>
      <td>250.0</td>
      <td>NaN</td>
      <td>22970500.0</td>
    </tr>
    <tr>
      <th>109</th>
      <td>Kobe Bryant</td>
      <td>Los Angeles Lakers</td>
      <td>24.0</td>
      <td>SF</td>
      <td>37.0</td>
      <td>6-6</td>
      <td>212.0</td>
      <td>NaN</td>
      <td>25000000.0</td>
    </tr>
  </tbody>
</table>
<p>458 rows × 9 columns</p>
</div>



#### 1.9. Sort a Data Frames with the .sort_values (   ), Method, Part II


```python
nba.sort_values(["Team", "Name"])
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>312</th>
      <td>Al Horford</td>
      <td>Atlanta Hawks</td>
      <td>15.0</td>
      <td>C</td>
      <td>30.0</td>
      <td>6-10</td>
      <td>245.0</td>
      <td>Florida</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>318</th>
      <td>Dennis Schroder</td>
      <td>Atlanta Hawks</td>
      <td>17.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-1</td>
      <td>172.0</td>
      <td>NaN</td>
      <td>1763400.0</td>
    </tr>
    <tr>
      <th>323</th>
      <td>Jeff Teague</td>
      <td>Atlanta Hawks</td>
      <td>0.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-2</td>
      <td>186.0</td>
      <td>Wake Forest</td>
      <td>8000000.0</td>
    </tr>
    <tr>
      <th>309</th>
      <td>Kent Bazemore</td>
      <td>Atlanta Hawks</td>
      <td>24.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-5</td>
      <td>201.0</td>
      <td>Old Dominion</td>
      <td>2000000.0</td>
    </tr>
    <tr>
      <th>311</th>
      <td>Kirk Hinrich</td>
      <td>Atlanta Hawks</td>
      <td>12.0</td>
      <td>SG</td>
      <td>35.0</td>
      <td>6-4</td>
      <td>190.0</td>
      <td>Kansas</td>
      <td>2854940.0</td>
    </tr>
    <tr>
      <th>313</th>
      <td>Kris Humphries</td>
      <td>Atlanta Hawks</td>
      <td>43.0</td>
      <td>PF</td>
      <td>31.0</td>
      <td>6-9</td>
      <td>235.0</td>
      <td>Minnesota</td>
      <td>1000000.0</td>
    </tr>
    <tr>
      <th>314</th>
      <td>Kyle Korver</td>
      <td>Atlanta Hawks</td>
      <td>26.0</td>
      <td>SG</td>
      <td>35.0</td>
      <td>6-7</td>
      <td>212.0</td>
      <td>Creighton</td>
      <td>5746479.0</td>
    </tr>
    <tr>
      <th>317</th>
      <td>Lamar Patterson</td>
      <td>Atlanta Hawks</td>
      <td>13.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-5</td>
      <td>225.0</td>
      <td>Pittsburgh</td>
      <td>525093.0</td>
    </tr>
    <tr>
      <th>316</th>
      <td>Mike Muscala</td>
      <td>Atlanta Hawks</td>
      <td>31.0</td>
      <td>PF</td>
      <td>24.0</td>
      <td>6-11</td>
      <td>240.0</td>
      <td>Bucknell</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>319</th>
      <td>Mike Scott</td>
      <td>Atlanta Hawks</td>
      <td>32.0</td>
      <td>PF</td>
      <td>27.0</td>
      <td>6-8</td>
      <td>237.0</td>
      <td>Virginia</td>
      <td>3333333.0</td>
    </tr>
    <tr>
      <th>315</th>
      <td>Paul Millsap</td>
      <td>Atlanta Hawks</td>
      <td>4.0</td>
      <td>PF</td>
      <td>31.0</td>
      <td>6-8</td>
      <td>246.0</td>
      <td>Louisiana Tech</td>
      <td>18671659.0</td>
    </tr>
    <tr>
      <th>320</th>
      <td>Thabo Sefolosha</td>
      <td>Atlanta Hawks</td>
      <td>25.0</td>
      <td>SF</td>
      <td>32.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>NaN</td>
      <td>4000000.0</td>
    </tr>
    <tr>
      <th>321</th>
      <td>Tiago Splitter</td>
      <td>Atlanta Hawks</td>
      <td>11.0</td>
      <td>C</td>
      <td>31.0</td>
      <td>6-11</td>
      <td>245.0</td>
      <td>NaN</td>
      <td>9756250.0</td>
    </tr>
    <tr>
      <th>310</th>
      <td>Tim Hardaway Jr.</td>
      <td>Atlanta Hawks</td>
      <td>10.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-6</td>
      <td>205.0</td>
      <td>Michigan</td>
      <td>1304520.0</td>
    </tr>
    <tr>
      <th>322</th>
      <td>Walter Tavares</td>
      <td>Atlanta Hawks</td>
      <td>22.0</td>
      <td>C</td>
      <td>24.0</td>
      <td>7-3</td>
      <td>260.0</td>
      <td>NaN</td>
      <td>1000000.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Amir Johnson</td>
      <td>Boston Celtics</td>
      <td>90.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Evan Turner</td>
      <td>Boston Celtics</td>
      <td>11.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>Ohio State</td>
      <td>3425510.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Isaiah Thomas</td>
      <td>Boston Celtics</td>
      <td>4.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>5-9</td>
      <td>185.0</td>
      <td>Washington</td>
      <td>6912869.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>James Young</td>
      <td>Boston Celtics</td>
      <td>13.0</td>
      <td>SG</td>
      <td>20.0</td>
      <td>6-6</td>
      <td>215.0</td>
      <td>Kentucky</td>
      <td>1749840.0</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Jared Sullinger</td>
      <td>Boston Celtics</td>
      <td>7.0</td>
      <td>C</td>
      <td>24.0</td>
      <td>6-9</td>
      <td>260.0</td>
      <td>Ohio State</td>
      <td>2569260.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Jordan Mickey</td>
      <td>Boston Celtics</td>
      <td>55.0</td>
      <td>PF</td>
      <td>21.0</td>
      <td>6-8</td>
      <td>235.0</td>
      <td>LSU</td>
      <td>1170960.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Kelly Olynyk</td>
      <td>Boston Celtics</td>
      <td>41.0</td>
      <td>C</td>
      <td>25.0</td>
      <td>7-0</td>
      <td>238.0</td>
      <td>Gonzaga</td>
      <td>2165160.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Marcus Smart</td>
      <td>Boston Celtics</td>
      <td>36.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-4</td>
      <td>220.0</td>
      <td>Oklahoma State</td>
      <td>3431040.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Terry Rozier</td>
      <td>Boston Celtics</td>
      <td>12.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-2</td>
      <td>190.0</td>
      <td>Louisville</td>
      <td>1824360.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Tyler Zeller</td>
      <td>Boston Celtics</td>
      <td>44.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>253.0</td>
      <td>North Carolina</td>
      <td>2616975.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>451</th>
      <td>Chris Johnson</td>
      <td>Utah Jazz</td>
      <td>23.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-6</td>
      <td>206.0</td>
      <td>Dayton</td>
      <td>981348.0</td>
    </tr>
    <tr>
      <th>445</th>
      <td>Dante Exum</td>
      <td>Utah Jazz</td>
      <td>11.0</td>
      <td>PG</td>
      <td>20.0</td>
      <td>6-6</td>
      <td>190.0</td>
      <td>NaN</td>
      <td>3777720.0</td>
    </tr>
    <tr>
      <th>446</th>
      <td>Derrick Favors</td>
      <td>Utah Jazz</td>
      <td>15.0</td>
      <td>PF</td>
      <td>24.0</td>
      <td>6-10</td>
      <td>265.0</td>
      <td>Georgia Tech</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>448</th>
      <td>Gordon Hayward</td>
      <td>Utah Jazz</td>
      <td>20.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-8</td>
      <td>226.0</td>
      <td>Butler</td>
      <td>15409570.0</td>
    </tr>
    <tr>
      <th>456</th>
      <td>Jeff Withey</td>
      <td>Utah Jazz</td>
      <td>24.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>231.0</td>
      <td>Kansas</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>450</th>
      <td>Joe Ingles</td>
      <td>Utah Jazz</td>
      <td>2.0</td>
      <td>SF</td>
      <td>28.0</td>
      <td>6-8</td>
      <td>226.0</td>
      <td>NaN</td>
      <td>2050000.0</td>
    </tr>
    <tr>
      <th>454</th>
      <td>Raul Neto</td>
      <td>Utah Jazz</td>
      <td>25.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-1</td>
      <td>179.0</td>
      <td>NaN</td>
      <td>900000.0</td>
    </tr>
    <tr>
      <th>449</th>
      <td>Rodney Hood</td>
      <td>Utah Jazz</td>
      <td>5.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-8</td>
      <td>206.0</td>
      <td>Duke</td>
      <td>1348440.0</td>
    </tr>
    <tr>
      <th>447</th>
      <td>Rudy Gobert</td>
      <td>Utah Jazz</td>
      <td>27.0</td>
      <td>C</td>
      <td>23.0</td>
      <td>7-1</td>
      <td>245.0</td>
      <td>NaN</td>
      <td>1175880.0</td>
    </tr>
    <tr>
      <th>453</th>
      <td>Shelvin Mack</td>
      <td>Utah Jazz</td>
      <td>8.0</td>
      <td>PG</td>
      <td>26.0</td>
      <td>6-3</td>
      <td>203.0</td>
      <td>Butler</td>
      <td>2433333.0</td>
    </tr>
    <tr>
      <th>455</th>
      <td>Tibor Pleiss</td>
      <td>Utah Jazz</td>
      <td>21.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-3</td>
      <td>256.0</td>
      <td>NaN</td>
      <td>2900000.0</td>
    </tr>
    <tr>
      <th>442</th>
      <td>Trevor Booker</td>
      <td>Utah Jazz</td>
      <td>33.0</td>
      <td>PF</td>
      <td>28.0</td>
      <td>6-8</td>
      <td>228.0</td>
      <td>Clemson</td>
      <td>4775000.0</td>
    </tr>
    <tr>
      <th>443</th>
      <td>Trey Burke</td>
      <td>Utah Jazz</td>
      <td>3.0</td>
      <td>PG</td>
      <td>23.0</td>
      <td>6-1</td>
      <td>191.0</td>
      <td>Michigan</td>
      <td>2658240.0</td>
    </tr>
    <tr>
      <th>452</th>
      <td>Trey Lyles</td>
      <td>Utah Jazz</td>
      <td>41.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-10</td>
      <td>234.0</td>
      <td>Kentucky</td>
      <td>2239800.0</td>
    </tr>
    <tr>
      <th>368</th>
      <td>Alan Anderson</td>
      <td>Washington Wizards</td>
      <td>6.0</td>
      <td>SG</td>
      <td>33.0</td>
      <td>6-6</td>
      <td>220.0</td>
      <td>Michigan State</td>
      <td>4000000.0</td>
    </tr>
    <tr>
      <th>369</th>
      <td>Bradley Beal</td>
      <td>Washington Wizards</td>
      <td>3.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>207.0</td>
      <td>Florida</td>
      <td>5694674.0</td>
    </tr>
    <tr>
      <th>372</th>
      <td>Drew Gooden</td>
      <td>Washington Wizards</td>
      <td>90.0</td>
      <td>PF</td>
      <td>34.0</td>
      <td>6-10</td>
      <td>250.0</td>
      <td>Kansas</td>
      <td>3300000.0</td>
    </tr>
    <tr>
      <th>380</th>
      <td>Garrett Temple</td>
      <td>Washington Wizards</td>
      <td>17.0</td>
      <td>SG</td>
      <td>30.0</td>
      <td>6-6</td>
      <td>195.0</td>
      <td>LSU</td>
      <td>1100602.0</td>
    </tr>
    <tr>
      <th>374</th>
      <td>JJ Hickson</td>
      <td>Washington Wizards</td>
      <td>21.0</td>
      <td>C</td>
      <td>27.0</td>
      <td>6-9</td>
      <td>242.0</td>
      <td>North Carolina State</td>
      <td>273038.0</td>
    </tr>
    <tr>
      <th>370</th>
      <td>Jared Dudley</td>
      <td>Washington Wizards</td>
      <td>1.0</td>
      <td>SF</td>
      <td>30.0</td>
      <td>6-7</td>
      <td>225.0</td>
      <td>Boston College</td>
      <td>4375000.0</td>
    </tr>
    <tr>
      <th>371</th>
      <td>Jarell Eddie</td>
      <td>Washington Wizards</td>
      <td>8.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-7</td>
      <td>218.0</td>
      <td>Virginia Tech</td>
      <td>561716.0</td>
    </tr>
    <tr>
      <th>382</th>
      <td>John Wall</td>
      <td>Washington Wizards</td>
      <td>2.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-4</td>
      <td>195.0</td>
      <td>Kentucky</td>
      <td>15851950.0</td>
    </tr>
    <tr>
      <th>377</th>
      <td>Kelly Oubre Jr.</td>
      <td>Washington Wizards</td>
      <td>12.0</td>
      <td>SF</td>
      <td>20.0</td>
      <td>6-7</td>
      <td>205.0</td>
      <td>Kansas</td>
      <td>1920240.0</td>
    </tr>
    <tr>
      <th>373</th>
      <td>Marcin Gortat</td>
      <td>Washington Wizards</td>
      <td>13.0</td>
      <td>C</td>
      <td>32.0</td>
      <td>6-11</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>11217391.0</td>
    </tr>
    <tr>
      <th>381</th>
      <td>Marcus Thornton</td>
      <td>Washington Wizards</td>
      <td>15.0</td>
      <td>SF</td>
      <td>29.0</td>
      <td>6-4</td>
      <td>205.0</td>
      <td>LSU</td>
      <td>200600.0</td>
    </tr>
    <tr>
      <th>376</th>
      <td>Markieff Morris</td>
      <td>Washington Wizards</td>
      <td>5.0</td>
      <td>PF</td>
      <td>26.0</td>
      <td>6-10</td>
      <td>245.0</td>
      <td>Kansas</td>
      <td>8000000.0</td>
    </tr>
    <tr>
      <th>375</th>
      <td>Nene Hilario</td>
      <td>Washington Wizards</td>
      <td>42.0</td>
      <td>C</td>
      <td>33.0</td>
      <td>6-11</td>
      <td>250.0</td>
      <td>NaN</td>
      <td>13000000.0</td>
    </tr>
    <tr>
      <th>378</th>
      <td>Otto Porter Jr.</td>
      <td>Washington Wizards</td>
      <td>22.0</td>
      <td>SF</td>
      <td>23.0</td>
      <td>6-8</td>
      <td>198.0</td>
      <td>Georgetown</td>
      <td>4662960.0</td>
    </tr>
    <tr>
      <th>379</th>
      <td>Ramon Sessions</td>
      <td>Washington Wizards</td>
      <td>7.0</td>
      <td>PG</td>
      <td>30.0</td>
      <td>6-3</td>
      <td>190.0</td>
      <td>Nevada</td>
      <td>2170465.0</td>
    </tr>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>458 rows × 9 columns</p>
</div>




```python
nba.sort_values(["Team", "Name"], ascending = False)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>379</th>
      <td>Ramon Sessions</td>
      <td>Washington Wizards</td>
      <td>7.0</td>
      <td>PG</td>
      <td>30.0</td>
      <td>6-3</td>
      <td>190.0</td>
      <td>Nevada</td>
      <td>2170465.0</td>
    </tr>
    <tr>
      <th>378</th>
      <td>Otto Porter Jr.</td>
      <td>Washington Wizards</td>
      <td>22.0</td>
      <td>SF</td>
      <td>23.0</td>
      <td>6-8</td>
      <td>198.0</td>
      <td>Georgetown</td>
      <td>4662960.0</td>
    </tr>
    <tr>
      <th>375</th>
      <td>Nene Hilario</td>
      <td>Washington Wizards</td>
      <td>42.0</td>
      <td>C</td>
      <td>33.0</td>
      <td>6-11</td>
      <td>250.0</td>
      <td>NaN</td>
      <td>13000000.0</td>
    </tr>
    <tr>
      <th>376</th>
      <td>Markieff Morris</td>
      <td>Washington Wizards</td>
      <td>5.0</td>
      <td>PF</td>
      <td>26.0</td>
      <td>6-10</td>
      <td>245.0</td>
      <td>Kansas</td>
      <td>8000000.0</td>
    </tr>
    <tr>
      <th>381</th>
      <td>Marcus Thornton</td>
      <td>Washington Wizards</td>
      <td>15.0</td>
      <td>SF</td>
      <td>29.0</td>
      <td>6-4</td>
      <td>205.0</td>
      <td>LSU</td>
      <td>200600.0</td>
    </tr>
    <tr>
      <th>373</th>
      <td>Marcin Gortat</td>
      <td>Washington Wizards</td>
      <td>13.0</td>
      <td>C</td>
      <td>32.0</td>
      <td>6-11</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>11217391.0</td>
    </tr>
    <tr>
      <th>377</th>
      <td>Kelly Oubre Jr.</td>
      <td>Washington Wizards</td>
      <td>12.0</td>
      <td>SF</td>
      <td>20.0</td>
      <td>6-7</td>
      <td>205.0</td>
      <td>Kansas</td>
      <td>1920240.0</td>
    </tr>
    <tr>
      <th>382</th>
      <td>John Wall</td>
      <td>Washington Wizards</td>
      <td>2.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-4</td>
      <td>195.0</td>
      <td>Kentucky</td>
      <td>15851950.0</td>
    </tr>
    <tr>
      <th>371</th>
      <td>Jarell Eddie</td>
      <td>Washington Wizards</td>
      <td>8.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-7</td>
      <td>218.0</td>
      <td>Virginia Tech</td>
      <td>561716.0</td>
    </tr>
    <tr>
      <th>370</th>
      <td>Jared Dudley</td>
      <td>Washington Wizards</td>
      <td>1.0</td>
      <td>SF</td>
      <td>30.0</td>
      <td>6-7</td>
      <td>225.0</td>
      <td>Boston College</td>
      <td>4375000.0</td>
    </tr>
    <tr>
      <th>374</th>
      <td>JJ Hickson</td>
      <td>Washington Wizards</td>
      <td>21.0</td>
      <td>C</td>
      <td>27.0</td>
      <td>6-9</td>
      <td>242.0</td>
      <td>North Carolina State</td>
      <td>273038.0</td>
    </tr>
    <tr>
      <th>380</th>
      <td>Garrett Temple</td>
      <td>Washington Wizards</td>
      <td>17.0</td>
      <td>SG</td>
      <td>30.0</td>
      <td>6-6</td>
      <td>195.0</td>
      <td>LSU</td>
      <td>1100602.0</td>
    </tr>
    <tr>
      <th>372</th>
      <td>Drew Gooden</td>
      <td>Washington Wizards</td>
      <td>90.0</td>
      <td>PF</td>
      <td>34.0</td>
      <td>6-10</td>
      <td>250.0</td>
      <td>Kansas</td>
      <td>3300000.0</td>
    </tr>
    <tr>
      <th>369</th>
      <td>Bradley Beal</td>
      <td>Washington Wizards</td>
      <td>3.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>207.0</td>
      <td>Florida</td>
      <td>5694674.0</td>
    </tr>
    <tr>
      <th>368</th>
      <td>Alan Anderson</td>
      <td>Washington Wizards</td>
      <td>6.0</td>
      <td>SG</td>
      <td>33.0</td>
      <td>6-6</td>
      <td>220.0</td>
      <td>Michigan State</td>
      <td>4000000.0</td>
    </tr>
    <tr>
      <th>452</th>
      <td>Trey Lyles</td>
      <td>Utah Jazz</td>
      <td>41.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-10</td>
      <td>234.0</td>
      <td>Kentucky</td>
      <td>2239800.0</td>
    </tr>
    <tr>
      <th>443</th>
      <td>Trey Burke</td>
      <td>Utah Jazz</td>
      <td>3.0</td>
      <td>PG</td>
      <td>23.0</td>
      <td>6-1</td>
      <td>191.0</td>
      <td>Michigan</td>
      <td>2658240.0</td>
    </tr>
    <tr>
      <th>442</th>
      <td>Trevor Booker</td>
      <td>Utah Jazz</td>
      <td>33.0</td>
      <td>PF</td>
      <td>28.0</td>
      <td>6-8</td>
      <td>228.0</td>
      <td>Clemson</td>
      <td>4775000.0</td>
    </tr>
    <tr>
      <th>455</th>
      <td>Tibor Pleiss</td>
      <td>Utah Jazz</td>
      <td>21.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-3</td>
      <td>256.0</td>
      <td>NaN</td>
      <td>2900000.0</td>
    </tr>
    <tr>
      <th>453</th>
      <td>Shelvin Mack</td>
      <td>Utah Jazz</td>
      <td>8.0</td>
      <td>PG</td>
      <td>26.0</td>
      <td>6-3</td>
      <td>203.0</td>
      <td>Butler</td>
      <td>2433333.0</td>
    </tr>
    <tr>
      <th>447</th>
      <td>Rudy Gobert</td>
      <td>Utah Jazz</td>
      <td>27.0</td>
      <td>C</td>
      <td>23.0</td>
      <td>7-1</td>
      <td>245.0</td>
      <td>NaN</td>
      <td>1175880.0</td>
    </tr>
    <tr>
      <th>449</th>
      <td>Rodney Hood</td>
      <td>Utah Jazz</td>
      <td>5.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-8</td>
      <td>206.0</td>
      <td>Duke</td>
      <td>1348440.0</td>
    </tr>
    <tr>
      <th>454</th>
      <td>Raul Neto</td>
      <td>Utah Jazz</td>
      <td>25.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-1</td>
      <td>179.0</td>
      <td>NaN</td>
      <td>900000.0</td>
    </tr>
    <tr>
      <th>450</th>
      <td>Joe Ingles</td>
      <td>Utah Jazz</td>
      <td>2.0</td>
      <td>SF</td>
      <td>28.0</td>
      <td>6-8</td>
      <td>226.0</td>
      <td>NaN</td>
      <td>2050000.0</td>
    </tr>
    <tr>
      <th>456</th>
      <td>Jeff Withey</td>
      <td>Utah Jazz</td>
      <td>24.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>231.0</td>
      <td>Kansas</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>448</th>
      <td>Gordon Hayward</td>
      <td>Utah Jazz</td>
      <td>20.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-8</td>
      <td>226.0</td>
      <td>Butler</td>
      <td>15409570.0</td>
    </tr>
    <tr>
      <th>446</th>
      <td>Derrick Favors</td>
      <td>Utah Jazz</td>
      <td>15.0</td>
      <td>PF</td>
      <td>24.0</td>
      <td>6-10</td>
      <td>265.0</td>
      <td>Georgia Tech</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>445</th>
      <td>Dante Exum</td>
      <td>Utah Jazz</td>
      <td>11.0</td>
      <td>PG</td>
      <td>20.0</td>
      <td>6-6</td>
      <td>190.0</td>
      <td>NaN</td>
      <td>3777720.0</td>
    </tr>
    <tr>
      <th>451</th>
      <td>Chris Johnson</td>
      <td>Utah Jazz</td>
      <td>23.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-6</td>
      <td>206.0</td>
      <td>Dayton</td>
      <td>981348.0</td>
    </tr>
    <tr>
      <th>444</th>
      <td>Alec Burks</td>
      <td>Utah Jazz</td>
      <td>10.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-6</td>
      <td>214.0</td>
      <td>Colorado</td>
      <td>9463484.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Terry Rozier</td>
      <td>Boston Celtics</td>
      <td>12.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-2</td>
      <td>190.0</td>
      <td>Louisville</td>
      <td>1824360.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Marcus Smart</td>
      <td>Boston Celtics</td>
      <td>36.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-4</td>
      <td>220.0</td>
      <td>Oklahoma State</td>
      <td>3431040.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Kelly Olynyk</td>
      <td>Boston Celtics</td>
      <td>41.0</td>
      <td>C</td>
      <td>25.0</td>
      <td>7-0</td>
      <td>238.0</td>
      <td>Gonzaga</td>
      <td>2165160.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Jordan Mickey</td>
      <td>Boston Celtics</td>
      <td>55.0</td>
      <td>PF</td>
      <td>21.0</td>
      <td>6-8</td>
      <td>235.0</td>
      <td>LSU</td>
      <td>1170960.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Jared Sullinger</td>
      <td>Boston Celtics</td>
      <td>7.0</td>
      <td>C</td>
      <td>24.0</td>
      <td>6-9</td>
      <td>260.0</td>
      <td>Ohio State</td>
      <td>2569260.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>James Young</td>
      <td>Boston Celtics</td>
      <td>13.0</td>
      <td>SG</td>
      <td>20.0</td>
      <td>6-6</td>
      <td>215.0</td>
      <td>Kentucky</td>
      <td>1749840.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Isaiah Thomas</td>
      <td>Boston Celtics</td>
      <td>4.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>5-9</td>
      <td>185.0</td>
      <td>Washington</td>
      <td>6912869.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Evan Turner</td>
      <td>Boston Celtics</td>
      <td>11.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>Ohio State</td>
      <td>3425510.0</td>
    </tr>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Amir Johnson</td>
      <td>Boston Celtics</td>
      <td>90.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>322</th>
      <td>Walter Tavares</td>
      <td>Atlanta Hawks</td>
      <td>22.0</td>
      <td>C</td>
      <td>24.0</td>
      <td>7-3</td>
      <td>260.0</td>
      <td>NaN</td>
      <td>1000000.0</td>
    </tr>
    <tr>
      <th>310</th>
      <td>Tim Hardaway Jr.</td>
      <td>Atlanta Hawks</td>
      <td>10.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-6</td>
      <td>205.0</td>
      <td>Michigan</td>
      <td>1304520.0</td>
    </tr>
    <tr>
      <th>321</th>
      <td>Tiago Splitter</td>
      <td>Atlanta Hawks</td>
      <td>11.0</td>
      <td>C</td>
      <td>31.0</td>
      <td>6-11</td>
      <td>245.0</td>
      <td>NaN</td>
      <td>9756250.0</td>
    </tr>
    <tr>
      <th>320</th>
      <td>Thabo Sefolosha</td>
      <td>Atlanta Hawks</td>
      <td>25.0</td>
      <td>SF</td>
      <td>32.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>NaN</td>
      <td>4000000.0</td>
    </tr>
    <tr>
      <th>315</th>
      <td>Paul Millsap</td>
      <td>Atlanta Hawks</td>
      <td>4.0</td>
      <td>PF</td>
      <td>31.0</td>
      <td>6-8</td>
      <td>246.0</td>
      <td>Louisiana Tech</td>
      <td>18671659.0</td>
    </tr>
    <tr>
      <th>319</th>
      <td>Mike Scott</td>
      <td>Atlanta Hawks</td>
      <td>32.0</td>
      <td>PF</td>
      <td>27.0</td>
      <td>6-8</td>
      <td>237.0</td>
      <td>Virginia</td>
      <td>3333333.0</td>
    </tr>
    <tr>
      <th>316</th>
      <td>Mike Muscala</td>
      <td>Atlanta Hawks</td>
      <td>31.0</td>
      <td>PF</td>
      <td>24.0</td>
      <td>6-11</td>
      <td>240.0</td>
      <td>Bucknell</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>317</th>
      <td>Lamar Patterson</td>
      <td>Atlanta Hawks</td>
      <td>13.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-5</td>
      <td>225.0</td>
      <td>Pittsburgh</td>
      <td>525093.0</td>
    </tr>
    <tr>
      <th>314</th>
      <td>Kyle Korver</td>
      <td>Atlanta Hawks</td>
      <td>26.0</td>
      <td>SG</td>
      <td>35.0</td>
      <td>6-7</td>
      <td>212.0</td>
      <td>Creighton</td>
      <td>5746479.0</td>
    </tr>
    <tr>
      <th>313</th>
      <td>Kris Humphries</td>
      <td>Atlanta Hawks</td>
      <td>43.0</td>
      <td>PF</td>
      <td>31.0</td>
      <td>6-9</td>
      <td>235.0</td>
      <td>Minnesota</td>
      <td>1000000.0</td>
    </tr>
    <tr>
      <th>311</th>
      <td>Kirk Hinrich</td>
      <td>Atlanta Hawks</td>
      <td>12.0</td>
      <td>SG</td>
      <td>35.0</td>
      <td>6-4</td>
      <td>190.0</td>
      <td>Kansas</td>
      <td>2854940.0</td>
    </tr>
    <tr>
      <th>309</th>
      <td>Kent Bazemore</td>
      <td>Atlanta Hawks</td>
      <td>24.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-5</td>
      <td>201.0</td>
      <td>Old Dominion</td>
      <td>2000000.0</td>
    </tr>
    <tr>
      <th>323</th>
      <td>Jeff Teague</td>
      <td>Atlanta Hawks</td>
      <td>0.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-2</td>
      <td>186.0</td>
      <td>Wake Forest</td>
      <td>8000000.0</td>
    </tr>
    <tr>
      <th>318</th>
      <td>Dennis Schroder</td>
      <td>Atlanta Hawks</td>
      <td>17.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-1</td>
      <td>172.0</td>
      <td>NaN</td>
      <td>1763400.0</td>
    </tr>
    <tr>
      <th>312</th>
      <td>Al Horford</td>
      <td>Atlanta Hawks</td>
      <td>15.0</td>
      <td>C</td>
      <td>30.0</td>
      <td>6-10</td>
      <td>245.0</td>
      <td>Florida</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>458 rows × 9 columns</p>
</div>




```python
nba.sort_values(["Team", "Name"], ascending = [True, False])
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>322</th>
      <td>Walter Tavares</td>
      <td>Atlanta Hawks</td>
      <td>22.0</td>
      <td>C</td>
      <td>24.0</td>
      <td>7-3</td>
      <td>260.0</td>
      <td>NaN</td>
      <td>1000000.0</td>
    </tr>
    <tr>
      <th>310</th>
      <td>Tim Hardaway Jr.</td>
      <td>Atlanta Hawks</td>
      <td>10.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-6</td>
      <td>205.0</td>
      <td>Michigan</td>
      <td>1304520.0</td>
    </tr>
    <tr>
      <th>321</th>
      <td>Tiago Splitter</td>
      <td>Atlanta Hawks</td>
      <td>11.0</td>
      <td>C</td>
      <td>31.0</td>
      <td>6-11</td>
      <td>245.0</td>
      <td>NaN</td>
      <td>9756250.0</td>
    </tr>
    <tr>
      <th>320</th>
      <td>Thabo Sefolosha</td>
      <td>Atlanta Hawks</td>
      <td>25.0</td>
      <td>SF</td>
      <td>32.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>NaN</td>
      <td>4000000.0</td>
    </tr>
    <tr>
      <th>315</th>
      <td>Paul Millsap</td>
      <td>Atlanta Hawks</td>
      <td>4.0</td>
      <td>PF</td>
      <td>31.0</td>
      <td>6-8</td>
      <td>246.0</td>
      <td>Louisiana Tech</td>
      <td>18671659.0</td>
    </tr>
    <tr>
      <th>319</th>
      <td>Mike Scott</td>
      <td>Atlanta Hawks</td>
      <td>32.0</td>
      <td>PF</td>
      <td>27.0</td>
      <td>6-8</td>
      <td>237.0</td>
      <td>Virginia</td>
      <td>3333333.0</td>
    </tr>
    <tr>
      <th>316</th>
      <td>Mike Muscala</td>
      <td>Atlanta Hawks</td>
      <td>31.0</td>
      <td>PF</td>
      <td>24.0</td>
      <td>6-11</td>
      <td>240.0</td>
      <td>Bucknell</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>317</th>
      <td>Lamar Patterson</td>
      <td>Atlanta Hawks</td>
      <td>13.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-5</td>
      <td>225.0</td>
      <td>Pittsburgh</td>
      <td>525093.0</td>
    </tr>
    <tr>
      <th>314</th>
      <td>Kyle Korver</td>
      <td>Atlanta Hawks</td>
      <td>26.0</td>
      <td>SG</td>
      <td>35.0</td>
      <td>6-7</td>
      <td>212.0</td>
      <td>Creighton</td>
      <td>5746479.0</td>
    </tr>
    <tr>
      <th>313</th>
      <td>Kris Humphries</td>
      <td>Atlanta Hawks</td>
      <td>43.0</td>
      <td>PF</td>
      <td>31.0</td>
      <td>6-9</td>
      <td>235.0</td>
      <td>Minnesota</td>
      <td>1000000.0</td>
    </tr>
    <tr>
      <th>311</th>
      <td>Kirk Hinrich</td>
      <td>Atlanta Hawks</td>
      <td>12.0</td>
      <td>SG</td>
      <td>35.0</td>
      <td>6-4</td>
      <td>190.0</td>
      <td>Kansas</td>
      <td>2854940.0</td>
    </tr>
    <tr>
      <th>309</th>
      <td>Kent Bazemore</td>
      <td>Atlanta Hawks</td>
      <td>24.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-5</td>
      <td>201.0</td>
      <td>Old Dominion</td>
      <td>2000000.0</td>
    </tr>
    <tr>
      <th>323</th>
      <td>Jeff Teague</td>
      <td>Atlanta Hawks</td>
      <td>0.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-2</td>
      <td>186.0</td>
      <td>Wake Forest</td>
      <td>8000000.0</td>
    </tr>
    <tr>
      <th>318</th>
      <td>Dennis Schroder</td>
      <td>Atlanta Hawks</td>
      <td>17.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-1</td>
      <td>172.0</td>
      <td>NaN</td>
      <td>1763400.0</td>
    </tr>
    <tr>
      <th>312</th>
      <td>Al Horford</td>
      <td>Atlanta Hawks</td>
      <td>15.0</td>
      <td>C</td>
      <td>30.0</td>
      <td>6-10</td>
      <td>245.0</td>
      <td>Florida</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Tyler Zeller</td>
      <td>Boston Celtics</td>
      <td>44.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>253.0</td>
      <td>North Carolina</td>
      <td>2616975.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Terry Rozier</td>
      <td>Boston Celtics</td>
      <td>12.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-2</td>
      <td>190.0</td>
      <td>Louisville</td>
      <td>1824360.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Marcus Smart</td>
      <td>Boston Celtics</td>
      <td>36.0</td>
      <td>PG</td>
      <td>22.0</td>
      <td>6-4</td>
      <td>220.0</td>
      <td>Oklahoma State</td>
      <td>3431040.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Kelly Olynyk</td>
      <td>Boston Celtics</td>
      <td>41.0</td>
      <td>C</td>
      <td>25.0</td>
      <td>7-0</td>
      <td>238.0</td>
      <td>Gonzaga</td>
      <td>2165160.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Jordan Mickey</td>
      <td>Boston Celtics</td>
      <td>55.0</td>
      <td>PF</td>
      <td>21.0</td>
      <td>6-8</td>
      <td>235.0</td>
      <td>LSU</td>
      <td>1170960.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Jared Sullinger</td>
      <td>Boston Celtics</td>
      <td>7.0</td>
      <td>C</td>
      <td>24.0</td>
      <td>6-9</td>
      <td>260.0</td>
      <td>Ohio State</td>
      <td>2569260.0</td>
    </tr>
    <tr>
      <th>13</th>
      <td>James Young</td>
      <td>Boston Celtics</td>
      <td>13.0</td>
      <td>SG</td>
      <td>20.0</td>
      <td>6-6</td>
      <td>215.0</td>
      <td>Kentucky</td>
      <td>1749840.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>11</th>
      <td>Isaiah Thomas</td>
      <td>Boston Celtics</td>
      <td>4.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>5-9</td>
      <td>185.0</td>
      <td>Washington</td>
      <td>6912869.0</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Evan Turner</td>
      <td>Boston Celtics</td>
      <td>11.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>Ohio State</td>
      <td>3425510.0</td>
    </tr>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Amir Johnson</td>
      <td>Boston Celtics</td>
      <td>90.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>443</th>
      <td>Trey Burke</td>
      <td>Utah Jazz</td>
      <td>3.0</td>
      <td>PG</td>
      <td>23.0</td>
      <td>6-1</td>
      <td>191.0</td>
      <td>Michigan</td>
      <td>2658240.0</td>
    </tr>
    <tr>
      <th>442</th>
      <td>Trevor Booker</td>
      <td>Utah Jazz</td>
      <td>33.0</td>
      <td>PF</td>
      <td>28.0</td>
      <td>6-8</td>
      <td>228.0</td>
      <td>Clemson</td>
      <td>4775000.0</td>
    </tr>
    <tr>
      <th>455</th>
      <td>Tibor Pleiss</td>
      <td>Utah Jazz</td>
      <td>21.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-3</td>
      <td>256.0</td>
      <td>NaN</td>
      <td>2900000.0</td>
    </tr>
    <tr>
      <th>453</th>
      <td>Shelvin Mack</td>
      <td>Utah Jazz</td>
      <td>8.0</td>
      <td>PG</td>
      <td>26.0</td>
      <td>6-3</td>
      <td>203.0</td>
      <td>Butler</td>
      <td>2433333.0</td>
    </tr>
    <tr>
      <th>447</th>
      <td>Rudy Gobert</td>
      <td>Utah Jazz</td>
      <td>27.0</td>
      <td>C</td>
      <td>23.0</td>
      <td>7-1</td>
      <td>245.0</td>
      <td>NaN</td>
      <td>1175880.0</td>
    </tr>
    <tr>
      <th>449</th>
      <td>Rodney Hood</td>
      <td>Utah Jazz</td>
      <td>5.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-8</td>
      <td>206.0</td>
      <td>Duke</td>
      <td>1348440.0</td>
    </tr>
    <tr>
      <th>454</th>
      <td>Raul Neto</td>
      <td>Utah Jazz</td>
      <td>25.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-1</td>
      <td>179.0</td>
      <td>NaN</td>
      <td>900000.0</td>
    </tr>
    <tr>
      <th>450</th>
      <td>Joe Ingles</td>
      <td>Utah Jazz</td>
      <td>2.0</td>
      <td>SF</td>
      <td>28.0</td>
      <td>6-8</td>
      <td>226.0</td>
      <td>NaN</td>
      <td>2050000.0</td>
    </tr>
    <tr>
      <th>456</th>
      <td>Jeff Withey</td>
      <td>Utah Jazz</td>
      <td>24.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>231.0</td>
      <td>Kansas</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>448</th>
      <td>Gordon Hayward</td>
      <td>Utah Jazz</td>
      <td>20.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-8</td>
      <td>226.0</td>
      <td>Butler</td>
      <td>15409570.0</td>
    </tr>
    <tr>
      <th>446</th>
      <td>Derrick Favors</td>
      <td>Utah Jazz</td>
      <td>15.0</td>
      <td>PF</td>
      <td>24.0</td>
      <td>6-10</td>
      <td>265.0</td>
      <td>Georgia Tech</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>445</th>
      <td>Dante Exum</td>
      <td>Utah Jazz</td>
      <td>11.0</td>
      <td>PG</td>
      <td>20.0</td>
      <td>6-6</td>
      <td>190.0</td>
      <td>NaN</td>
      <td>3777720.0</td>
    </tr>
    <tr>
      <th>451</th>
      <td>Chris Johnson</td>
      <td>Utah Jazz</td>
      <td>23.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-6</td>
      <td>206.0</td>
      <td>Dayton</td>
      <td>981348.0</td>
    </tr>
    <tr>
      <th>444</th>
      <td>Alec Burks</td>
      <td>Utah Jazz</td>
      <td>10.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-6</td>
      <td>214.0</td>
      <td>Colorado</td>
      <td>9463484.0</td>
    </tr>
    <tr>
      <th>379</th>
      <td>Ramon Sessions</td>
      <td>Washington Wizards</td>
      <td>7.0</td>
      <td>PG</td>
      <td>30.0</td>
      <td>6-3</td>
      <td>190.0</td>
      <td>Nevada</td>
      <td>2170465.0</td>
    </tr>
    <tr>
      <th>378</th>
      <td>Otto Porter Jr.</td>
      <td>Washington Wizards</td>
      <td>22.0</td>
      <td>SF</td>
      <td>23.0</td>
      <td>6-8</td>
      <td>198.0</td>
      <td>Georgetown</td>
      <td>4662960.0</td>
    </tr>
    <tr>
      <th>375</th>
      <td>Nene Hilario</td>
      <td>Washington Wizards</td>
      <td>42.0</td>
      <td>C</td>
      <td>33.0</td>
      <td>6-11</td>
      <td>250.0</td>
      <td>NaN</td>
      <td>13000000.0</td>
    </tr>
    <tr>
      <th>376</th>
      <td>Markieff Morris</td>
      <td>Washington Wizards</td>
      <td>5.0</td>
      <td>PF</td>
      <td>26.0</td>
      <td>6-10</td>
      <td>245.0</td>
      <td>Kansas</td>
      <td>8000000.0</td>
    </tr>
    <tr>
      <th>381</th>
      <td>Marcus Thornton</td>
      <td>Washington Wizards</td>
      <td>15.0</td>
      <td>SF</td>
      <td>29.0</td>
      <td>6-4</td>
      <td>205.0</td>
      <td>LSU</td>
      <td>200600.0</td>
    </tr>
    <tr>
      <th>373</th>
      <td>Marcin Gortat</td>
      <td>Washington Wizards</td>
      <td>13.0</td>
      <td>C</td>
      <td>32.0</td>
      <td>6-11</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>11217391.0</td>
    </tr>
    <tr>
      <th>377</th>
      <td>Kelly Oubre Jr.</td>
      <td>Washington Wizards</td>
      <td>12.0</td>
      <td>SF</td>
      <td>20.0</td>
      <td>6-7</td>
      <td>205.0</td>
      <td>Kansas</td>
      <td>1920240.0</td>
    </tr>
    <tr>
      <th>382</th>
      <td>John Wall</td>
      <td>Washington Wizards</td>
      <td>2.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-4</td>
      <td>195.0</td>
      <td>Kentucky</td>
      <td>15851950.0</td>
    </tr>
    <tr>
      <th>371</th>
      <td>Jarell Eddie</td>
      <td>Washington Wizards</td>
      <td>8.0</td>
      <td>SG</td>
      <td>24.0</td>
      <td>6-7</td>
      <td>218.0</td>
      <td>Virginia Tech</td>
      <td>561716.0</td>
    </tr>
    <tr>
      <th>370</th>
      <td>Jared Dudley</td>
      <td>Washington Wizards</td>
      <td>1.0</td>
      <td>SF</td>
      <td>30.0</td>
      <td>6-7</td>
      <td>225.0</td>
      <td>Boston College</td>
      <td>4375000.0</td>
    </tr>
    <tr>
      <th>374</th>
      <td>JJ Hickson</td>
      <td>Washington Wizards</td>
      <td>21.0</td>
      <td>C</td>
      <td>27.0</td>
      <td>6-9</td>
      <td>242.0</td>
      <td>North Carolina State</td>
      <td>273038.0</td>
    </tr>
    <tr>
      <th>380</th>
      <td>Garrett Temple</td>
      <td>Washington Wizards</td>
      <td>17.0</td>
      <td>SG</td>
      <td>30.0</td>
      <td>6-6</td>
      <td>195.0</td>
      <td>LSU</td>
      <td>1100602.0</td>
    </tr>
    <tr>
      <th>372</th>
      <td>Drew Gooden</td>
      <td>Washington Wizards</td>
      <td>90.0</td>
      <td>PF</td>
      <td>34.0</td>
      <td>6-10</td>
      <td>250.0</td>
      <td>Kansas</td>
      <td>3300000.0</td>
    </tr>
    <tr>
      <th>369</th>
      <td>Bradley Beal</td>
      <td>Washington Wizards</td>
      <td>3.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>207.0</td>
      <td>Florida</td>
      <td>5694674.0</td>
    </tr>
    <tr>
      <th>368</th>
      <td>Alan Anderson</td>
      <td>Washington Wizards</td>
      <td>6.0</td>
      <td>SG</td>
      <td>33.0</td>
      <td>6-6</td>
      <td>220.0</td>
      <td>Michigan State</td>
      <td>4000000.0</td>
    </tr>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
<p>458 rows × 9 columns</p>
</div>




```python
nba = pd.read_csv("nba.csv")
nba.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.sort_values(["Number", "Salary", "Name"], inplace = True)
nba.tail()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>372</th>
      <td>Drew Gooden</td>
      <td>Washington Wizards</td>
      <td>90.0</td>
      <td>PF</td>
      <td>34.0</td>
      <td>6-10</td>
      <td>250.0</td>
      <td>Kansas</td>
      <td>3300000.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Amir Johnson</td>
      <td>Boston Celtics</td>
      <td>90.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>NaN</td>
      <td>12000000.0</td>
    </tr>
    <tr>
      <th>68</th>
      <td>Lucas Nogueira</td>
      <td>Toronto Raptors</td>
      <td>92.0</td>
      <td>C</td>
      <td>23.0</td>
      <td>7-0</td>
      <td>220.0</td>
      <td>NaN</td>
      <td>1842000.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117.0</td>
    </tr>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.sort_index(ascending = False).head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>457</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>456</th>
      <td>Jeff Withey</td>
      <td>Utah Jazz</td>
      <td>24.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-0</td>
      <td>231.0</td>
      <td>Kansas</td>
      <td>947276.0</td>
    </tr>
    <tr>
      <th>455</th>
      <td>Tibor Pleiss</td>
      <td>Utah Jazz</td>
      <td>21.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>7-3</td>
      <td>256.0</td>
      <td>NaN</td>
      <td>2900000.0</td>
    </tr>
    <tr>
      <th>454</th>
      <td>Raul Neto</td>
      <td>Utah Jazz</td>
      <td>25.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-1</td>
      <td>179.0</td>
      <td>NaN</td>
      <td>900000.0</td>
    </tr>
    <tr>
      <th>453</th>
      <td>Shelvin Mack</td>
      <td>Utah Jazz</td>
      <td>8.0</td>
      <td>PG</td>
      <td>26.0</td>
      <td>6-3</td>
      <td>203.0</td>
      <td>Butler</td>
      <td>2433333.0</td>
    </tr>
    <tr>
      <th>452</th>
      <td>Trey Lyles</td>
      <td>Utah Jazz</td>
      <td>41.0</td>
      <td>PF</td>
      <td>20.0</td>
      <td>6-10</td>
      <td>234.0</td>
      <td>Kentucky</td>
      <td>2239800.0</td>
    </tr>
    <tr>
      <th>451</th>
      <td>Chris Johnson</td>
      <td>Utah Jazz</td>
      <td>23.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-6</td>
      <td>206.0</td>
      <td>Dayton</td>
      <td>981348.0</td>
    </tr>
    <tr>
      <th>450</th>
      <td>Joe Ingles</td>
      <td>Utah Jazz</td>
      <td>2.0</td>
      <td>SF</td>
      <td>28.0</td>
      <td>6-8</td>
      <td>226.0</td>
      <td>NaN</td>
      <td>2050000.0</td>
    </tr>
    <tr>
      <th>449</th>
      <td>Rodney Hood</td>
      <td>Utah Jazz</td>
      <td>5.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-8</td>
      <td>206.0</td>
      <td>Duke</td>
      <td>1348440.0</td>
    </tr>
    <tr>
      <th>448</th>
      <td>Gordon Hayward</td>
      <td>Utah Jazz</td>
      <td>20.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-8</td>
      <td>226.0</td>
      <td>Butler</td>
      <td>15409570.0</td>
    </tr>
  </tbody>
</table>
</div>



#### 1.10.  Rank Values with .rank ( )  Method


```python
nba = pd.read_csv("nba.csv").dropna(how = "all")
nba["Salary"] = nba ["Salary"].fillna(0).astype("int")
nba.head(3)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>0</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Rank of Highest salary on NBA
nba["Salary Rank"] = nba["Salary"].rank(ascending = False).astype("int")
nba.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
      <th>Salary Rank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Avery Bradley</td>
      <td>Boston Celtics</td>
      <td>0.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>Texas</td>
      <td>7730337</td>
      <td>97</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Jae Crowder</td>
      <td>Boston Celtics</td>
      <td>99.0</td>
      <td>SF</td>
      <td>25.0</td>
      <td>6-6</td>
      <td>235.0</td>
      <td>Marquette</td>
      <td>6796117</td>
      <td>110</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>0</td>
      <td>452</td>
    </tr>
    <tr>
      <th>3</th>
      <td>R.J. Hunter</td>
      <td>Boston Celtics</td>
      <td>28.0</td>
      <td>SG</td>
      <td>22.0</td>
      <td>6-5</td>
      <td>185.0</td>
      <td>Georgia State</td>
      <td>1148640</td>
      <td>322</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Jonas Jerebko</td>
      <td>Boston Celtics</td>
      <td>8.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-10</td>
      <td>231.0</td>
      <td>NaN</td>
      <td>5000000</td>
      <td>147</td>
    </tr>
  </tbody>
</table>
</div>




```python
nba.sort_values(by = "Salary", ascending = False)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Name</th>
      <th>Team</th>
      <th>Number</th>
      <th>Position</th>
      <th>Age</th>
      <th>Height</th>
      <th>Weight</th>
      <th>College</th>
      <th>Salary</th>
      <th>Salary Rank</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>109</th>
      <td>Kobe Bryant</td>
      <td>Los Angeles Lakers</td>
      <td>24.0</td>
      <td>SF</td>
      <td>37.0</td>
      <td>6-6</td>
      <td>212.0</td>
      <td>NaN</td>
      <td>25000000</td>
      <td>1</td>
    </tr>
    <tr>
      <th>169</th>
      <td>LeBron James</td>
      <td>Cleveland Cavaliers</td>
      <td>23.0</td>
      <td>SF</td>
      <td>31.0</td>
      <td>6-8</td>
      <td>250.0</td>
      <td>NaN</td>
      <td>22970500</td>
      <td>2</td>
    </tr>
    <tr>
      <th>33</th>
      <td>Carmelo Anthony</td>
      <td>New York Knicks</td>
      <td>7.0</td>
      <td>SF</td>
      <td>32.0</td>
      <td>6-8</td>
      <td>240.0</td>
      <td>Syracuse</td>
      <td>22875000</td>
      <td>3</td>
    </tr>
    <tr>
      <th>251</th>
      <td>Dwight Howard</td>
      <td>Houston Rockets</td>
      <td>12.0</td>
      <td>C</td>
      <td>30.0</td>
      <td>6-11</td>
      <td>265.0</td>
      <td>NaN</td>
      <td>22359364</td>
      <td>4</td>
    </tr>
    <tr>
      <th>339</th>
      <td>Chris Bosh</td>
      <td>Miami Heat</td>
      <td>1.0</td>
      <td>PF</td>
      <td>32.0</td>
      <td>6-11</td>
      <td>235.0</td>
      <td>Georgia Tech</td>
      <td>22192730</td>
      <td>5</td>
    </tr>
    <tr>
      <th>100</th>
      <td>Chris Paul</td>
      <td>Los Angeles Clippers</td>
      <td>3.0</td>
      <td>PG</td>
      <td>31.0</td>
      <td>6-0</td>
      <td>175.0</td>
      <td>Wake Forest</td>
      <td>21468695</td>
      <td>6</td>
    </tr>
    <tr>
      <th>414</th>
      <td>Kevin Durant</td>
      <td>Oklahoma City Thunder</td>
      <td>35.0</td>
      <td>SF</td>
      <td>27.0</td>
      <td>6-9</td>
      <td>240.0</td>
      <td>Texas</td>
      <td>20158622</td>
      <td>7</td>
    </tr>
    <tr>
      <th>164</th>
      <td>Derrick Rose</td>
      <td>Chicago Bulls</td>
      <td>1.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-3</td>
      <td>190.0</td>
      <td>Memphis</td>
      <td>20093064</td>
      <td>8</td>
    </tr>
    <tr>
      <th>349</th>
      <td>Dwyane Wade</td>
      <td>Miami Heat</td>
      <td>3.0</td>
      <td>SG</td>
      <td>34.0</td>
      <td>6-4</td>
      <td>220.0</td>
      <td>Marquette</td>
      <td>20000000</td>
      <td>9</td>
    </tr>
    <tr>
      <th>174</th>
      <td>Kevin Love</td>
      <td>Cleveland Cavaliers</td>
      <td>0.0</td>
      <td>PF</td>
      <td>27.0</td>
      <td>6-10</td>
      <td>251.0</td>
      <td>UCLA</td>
      <td>19689000</td>
      <td>11</td>
    </tr>
    <tr>
      <th>98</th>
      <td>DeAndre Jordan</td>
      <td>Los Angeles Clippers</td>
      <td>6.0</td>
      <td>C</td>
      <td>27.0</td>
      <td>6-11</td>
      <td>265.0</td>
      <td>Texas A&amp;M</td>
      <td>19689000</td>
      <td>11</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Brook Lopez</td>
      <td>Brooklyn Nets</td>
      <td>11.0</td>
      <td>C</td>
      <td>28.0</td>
      <td>7-0</td>
      <td>275.0</td>
      <td>Stanford</td>
      <td>19689000</td>
      <td>11</td>
    </tr>
    <tr>
      <th>294</th>
      <td>LaMarcus Aldridge</td>
      <td>San Antonio Spurs</td>
      <td>12.0</td>
      <td>PF</td>
      <td>30.0</td>
      <td>6-11</td>
      <td>240.0</td>
      <td>Texas</td>
      <td>19689000</td>
      <td>11</td>
    </tr>
    <tr>
      <th>265</th>
      <td>Marc Gasol</td>
      <td>Memphis Grizzlies</td>
      <td>33.0</td>
      <td>C</td>
      <td>31.0</td>
      <td>7-1</td>
      <td>255.0</td>
      <td>NaN</td>
      <td>19688000</td>
      <td>14</td>
    </tr>
    <tr>
      <th>96</th>
      <td>Blake Griffin</td>
      <td>Los Angeles Clippers</td>
      <td>32.0</td>
      <td>PF</td>
      <td>27.0</td>
      <td>6-10</td>
      <td>251.0</td>
      <td>Oklahoma</td>
      <td>18907726</td>
      <td>15</td>
    </tr>
    <tr>
      <th>315</th>
      <td>Paul Millsap</td>
      <td>Atlanta Hawks</td>
      <td>4.0</td>
      <td>PF</td>
      <td>31.0</td>
      <td>6-8</td>
      <td>246.0</td>
      <td>Louisiana Tech</td>
      <td>18671659</td>
      <td>16</td>
    </tr>
    <tr>
      <th>199</th>
      <td>Paul George</td>
      <td>Indiana Pacers</td>
      <td>13.0</td>
      <td>SF</td>
      <td>26.0</td>
      <td>6-9</td>
      <td>220.0</td>
      <td>Fresno State</td>
      <td>17120106</td>
      <td>17</td>
    </tr>
    <tr>
      <th>426</th>
      <td>Russell Westbrook</td>
      <td>Oklahoma City Thunder</td>
      <td>0.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-3</td>
      <td>200.0</td>
      <td>UCLA</td>
      <td>16744218</td>
      <td>18</td>
    </tr>
    <tr>
      <th>168</th>
      <td>Kyrie Irving</td>
      <td>Cleveland Cavaliers</td>
      <td>2.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-3</td>
      <td>193.0</td>
      <td>Duke</td>
      <td>16407501</td>
      <td>19</td>
    </tr>
    <tr>
      <th>233</th>
      <td>Wesley Matthews</td>
      <td>Dallas Mavericks</td>
      <td>23.0</td>
      <td>SG</td>
      <td>29.0</td>
      <td>6-5</td>
      <td>220.0</td>
      <td>Marquette</td>
      <td>16407500</td>
      <td>22</td>
    </tr>
    <tr>
      <th>301</th>
      <td>Kawhi Leonard</td>
      <td>San Antonio Spurs</td>
      <td>2.0</td>
      <td>SF</td>
      <td>24.0</td>
      <td>6-7</td>
      <td>230.0</td>
      <td>San Diego State</td>
      <td>16407500</td>
      <td>22</td>
    </tr>
    <tr>
      <th>418</th>
      <td>Enes Kanter</td>
      <td>Oklahoma City Thunder</td>
      <td>11.0</td>
      <td>C</td>
      <td>24.0</td>
      <td>6-11</td>
      <td>245.0</td>
      <td>Kentucky</td>
      <td>16407500</td>
      <td>22</td>
    </tr>
    <tr>
      <th>153</th>
      <td>Jimmy Butler</td>
      <td>Chicago Bulls</td>
      <td>21.0</td>
      <td>SG</td>
      <td>26.0</td>
      <td>6-7</td>
      <td>220.0</td>
      <td>Marquette</td>
      <td>16407500</td>
      <td>22</td>
    </tr>
    <tr>
      <th>220</th>
      <td>Greg Monroe</td>
      <td>Milwaukee Bucks</td>
      <td>15.0</td>
      <td>C</td>
      <td>26.0</td>
      <td>6-11</td>
      <td>265.0</td>
      <td>Georgetown</td>
      <td>16407500</td>
      <td>22</td>
    </tr>
    <tr>
      <th>189</th>
      <td>Tobias Harris</td>
      <td>Detroit Pistons</td>
      <td>34.0</td>
      <td>SF</td>
      <td>23.0</td>
      <td>6-9</td>
      <td>235.0</td>
      <td>Tennessee</td>
      <td>16000000</td>
      <td>25</td>
    </tr>
    <tr>
      <th>382</th>
      <td>John Wall</td>
      <td>Washington Wizards</td>
      <td>2.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-4</td>
      <td>195.0</td>
      <td>Kentucky</td>
      <td>15851950</td>
      <td>26</td>
    </tr>
    <tr>
      <th>143</th>
      <td>DeMarcus Cousins</td>
      <td>Sacramento Kings</td>
      <td>15.0</td>
      <td>C</td>
      <td>25.0</td>
      <td>6-11</td>
      <td>270.0</td>
      <td>Kentucky</td>
      <td>15851950</td>
      <td>26</td>
    </tr>
    <tr>
      <th>249</th>
      <td>James Harden</td>
      <td>Houston Rockets</td>
      <td>13.0</td>
      <td>SG</td>
      <td>26.0</td>
      <td>6-5</td>
      <td>220.0</td>
      <td>Arizona State</td>
      <td>15756438</td>
      <td>28</td>
    </tr>
    <tr>
      <th>111</th>
      <td>Roy Hibbert</td>
      <td>Los Angeles Lakers</td>
      <td>17.0</td>
      <td>C</td>
      <td>29.0</td>
      <td>7-2</td>
      <td>270.0</td>
      <td>Georgetown</td>
      <td>15592217</td>
      <td>29</td>
    </tr>
    <tr>
      <th>288</th>
      <td>Eric Gordon</td>
      <td>New Orleans Pelicans</td>
      <td>10.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-4</td>
      <td>215.0</td>
      <td>Indiana</td>
      <td>15514031</td>
      <td>30</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>304</th>
      <td>Andre Miller</td>
      <td>San Antonio Spurs</td>
      <td>24.0</td>
      <td>PG</td>
      <td>40.0</td>
      <td>6-3</td>
      <td>200.0</td>
      <td>Utah</td>
      <td>250750</td>
      <td>428</td>
    </tr>
    <tr>
      <th>73</th>
      <td>Jason Thompson</td>
      <td>Toronto Raptors</td>
      <td>1.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-11</td>
      <td>250.0</td>
      <td>Rider</td>
      <td>245177</td>
      <td>429</td>
    </tr>
    <tr>
      <th>420</th>
      <td>Nazr Mohammed</td>
      <td>Oklahoma City Thunder</td>
      <td>13.0</td>
      <td>C</td>
      <td>38.0</td>
      <td>6-10</td>
      <td>250.0</td>
      <td>Kentucky</td>
      <td>222888</td>
      <td>430</td>
    </tr>
    <tr>
      <th>203</th>
      <td>Ty Lawson</td>
      <td>Indiana Pacers</td>
      <td>10.0</td>
      <td>PG</td>
      <td>28.0</td>
      <td>5-11</td>
      <td>195.0</td>
      <td>North Carolina</td>
      <td>211744</td>
      <td>431</td>
    </tr>
    <tr>
      <th>123</th>
      <td>Chase Budinger</td>
      <td>Phoenix Suns</td>
      <td>10.0</td>
      <td>SF</td>
      <td>28.0</td>
      <td>6-7</td>
      <td>209.0</td>
      <td>Arizona</td>
      <td>206192</td>
      <td>432</td>
    </tr>
    <tr>
      <th>248</th>
      <td>Andrew Goudelock</td>
      <td>Houston Rockets</td>
      <td>0.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-3</td>
      <td>200.0</td>
      <td>Charleston</td>
      <td>200600</td>
      <td>434</td>
    </tr>
    <tr>
      <th>381</th>
      <td>Marcus Thornton</td>
      <td>Washington Wizards</td>
      <td>15.0</td>
      <td>SF</td>
      <td>29.0</td>
      <td>6-4</td>
      <td>205.0</td>
      <td>LSU</td>
      <td>200600</td>
      <td>434</td>
    </tr>
    <tr>
      <th>303</th>
      <td>Kevin Martin</td>
      <td>San Antonio Spurs</td>
      <td>23.0</td>
      <td>SG</td>
      <td>33.0</td>
      <td>6-7</td>
      <td>199.0</td>
      <td>Western Carolina</td>
      <td>200600</td>
      <td>434</td>
    </tr>
    <tr>
      <th>326</th>
      <td>Jorge Gutierrez</td>
      <td>Charlotte Hornets</td>
      <td>12.0</td>
      <td>PG</td>
      <td>27.0</td>
      <td>6-3</td>
      <td>189.0</td>
      <td>California</td>
      <td>189455</td>
      <td>436</td>
    </tr>
    <tr>
      <th>282</th>
      <td>Bryce Dejean-Jones</td>
      <td>New Orleans Pelicans</td>
      <td>31.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-6</td>
      <td>203.0</td>
      <td>Iowa State</td>
      <td>169883</td>
      <td>437</td>
    </tr>
    <tr>
      <th>45</th>
      <td>Tony Wroten</td>
      <td>New York Knicks</td>
      <td>5.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-6</td>
      <td>205.0</td>
      <td>Washington</td>
      <td>167406</td>
      <td>438</td>
    </tr>
    <tr>
      <th>21</th>
      <td>Sean Kilpatrick</td>
      <td>Brooklyn Nets</td>
      <td>6.0</td>
      <td>SG</td>
      <td>26.0</td>
      <td>6-4</td>
      <td>219.0</td>
      <td>Cincinnati</td>
      <td>134215</td>
      <td>439</td>
    </tr>
    <tr>
      <th>92</th>
      <td>Jeff Ayres</td>
      <td>Los Angeles Clippers</td>
      <td>19.0</td>
      <td>PF</td>
      <td>29.0</td>
      <td>6-9</td>
      <td>250.0</td>
      <td>Arizona State</td>
      <td>111444</td>
      <td>440</td>
    </tr>
    <tr>
      <th>184</th>
      <td>Lorenzo Brown</td>
      <td>Detroit Pistons</td>
      <td>17.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>6-5</td>
      <td>189.0</td>
      <td>North Carolina State</td>
      <td>111444</td>
      <td>440</td>
    </tr>
    <tr>
      <th>175</th>
      <td>Jordan McRae</td>
      <td>Cleveland Cavaliers</td>
      <td>12.0</td>
      <td>SG</td>
      <td>25.0</td>
      <td>6-5</td>
      <td>179.0</td>
      <td>Tennessee</td>
      <td>111196</td>
      <td>442</td>
    </tr>
    <tr>
      <th>135</th>
      <td>Alan Williams</td>
      <td>Phoenix Suns</td>
      <td>15.0</td>
      <td>C</td>
      <td>23.0</td>
      <td>6-8</td>
      <td>260.0</td>
      <td>UC Santa Barbara</td>
      <td>83397</td>
      <td>443</td>
    </tr>
    <tr>
      <th>130</th>
      <td>Phil Pressey</td>
      <td>Phoenix Suns</td>
      <td>25.0</td>
      <td>PG</td>
      <td>25.0</td>
      <td>5-11</td>
      <td>175.0</td>
      <td>Missouri</td>
      <td>55722</td>
      <td>444</td>
    </tr>
    <tr>
      <th>291</th>
      <td>Orlando Johnson</td>
      <td>New Orleans Pelicans</td>
      <td>0.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>220.0</td>
      <td>UC Santa Barbara</td>
      <td>55722</td>
      <td>444</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Thanasis Antetokounmpo</td>
      <td>New York Knicks</td>
      <td>43.0</td>
      <td>SF</td>
      <td>23.0</td>
      <td>6-7</td>
      <td>205.0</td>
      <td>NaN</td>
      <td>30888</td>
      <td>446</td>
    </tr>
    <tr>
      <th>350</th>
      <td>Briante Weber</td>
      <td>Miami Heat</td>
      <td>12.0</td>
      <td>PG</td>
      <td>23.0</td>
      <td>6-2</td>
      <td>165.0</td>
      <td>Virginia Commonwealth</td>
      <td>0</td>
      <td>452</td>
    </tr>
    <tr>
      <th>46</th>
      <td>Elton Brand</td>
      <td>Philadelphia 76ers</td>
      <td>42.0</td>
      <td>PF</td>
      <td>37.0</td>
      <td>6-9</td>
      <td>254.0</td>
      <td>Duke</td>
      <td>0</td>
      <td>452</td>
    </tr>
    <tr>
      <th>2</th>
      <td>John Holland</td>
      <td>Boston Celtics</td>
      <td>30.0</td>
      <td>SG</td>
      <td>27.0</td>
      <td>6-5</td>
      <td>205.0</td>
      <td>Boston University</td>
      <td>0</td>
      <td>452</td>
    </tr>
    <tr>
      <th>171</th>
      <td>Dahntay Jones</td>
      <td>Cleveland Cavaliers</td>
      <td>30.0</td>
      <td>SG</td>
      <td>35.0</td>
      <td>6-6</td>
      <td>225.0</td>
      <td>Duke</td>
      <td>0</td>
      <td>452</td>
    </tr>
    <tr>
      <th>397</th>
      <td>Axel Toupane</td>
      <td>Denver Nuggets</td>
      <td>6.0</td>
      <td>SG</td>
      <td>23.0</td>
      <td>6-7</td>
      <td>210.0</td>
      <td>NaN</td>
      <td>0</td>
      <td>452</td>
    </tr>
    <tr>
      <th>269</th>
      <td>Ray McCallum</td>
      <td>Memphis Grizzlies</td>
      <td>5.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-3</td>
      <td>190.0</td>
      <td>Detroit</td>
      <td>0</td>
      <td>452</td>
    </tr>
    <tr>
      <th>353</th>
      <td>Dorell Wright</td>
      <td>Miami Heat</td>
      <td>11.0</td>
      <td>SF</td>
      <td>30.0</td>
      <td>6-9</td>
      <td>205.0</td>
      <td>NaN</td>
      <td>0</td>
      <td>452</td>
    </tr>
    <tr>
      <th>264</th>
      <td>Jordan Farmar</td>
      <td>Memphis Grizzlies</td>
      <td>4.0</td>
      <td>PG</td>
      <td>29.0</td>
      <td>6-2</td>
      <td>180.0</td>
      <td>UCLA</td>
      <td>0</td>
      <td>452</td>
    </tr>
    <tr>
      <th>409</th>
      <td>Greg Smith</td>
      <td>Minnesota Timberwolves</td>
      <td>4.0</td>
      <td>PF</td>
      <td>25.0</td>
      <td>6-10</td>
      <td>250.0</td>
      <td>Fresno State</td>
      <td>0</td>
      <td>452</td>
    </tr>
    <tr>
      <th>273</th>
      <td>Alex Stepheson</td>
      <td>Memphis Grizzlies</td>
      <td>35.0</td>
      <td>PF</td>
      <td>28.0</td>
      <td>6-10</td>
      <td>270.0</td>
      <td>USC</td>
      <td>0</td>
      <td>452</td>
    </tr>
    <tr>
      <th>270</th>
      <td>Xavier Munford</td>
      <td>Memphis Grizzlies</td>
      <td>14.0</td>
      <td>PG</td>
      <td>24.0</td>
      <td>6-3</td>
      <td>180.0</td>
      <td>Rhode Island</td>
      <td>0</td>
      <td>452</td>
    </tr>
  </tbody>
</table>
<p>457 rows × 10 columns</p>
</div>




```python

```


```python

```
