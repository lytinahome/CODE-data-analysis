# Cheet sheet for Pandas


## concat and append
```python
pd.concat(objs, axis=0, join='outer', join_axes=None, ignore_index=False,
          keys=None, levels=None, names=None, verify_integrity=False,
          copy=True)
```
``pd.concat(df1, df2)`` is equalivent to ``df1.append(df2)``

## merge and join
```python
pd.merge(left, right, how='inner', on=None, left_on=None, right_on=None,
         left_index=False, right_index=False, sort=True,
         suffixes=('_x', '_y'), copy=True, indicator=False,
         validate=None)
```
``pd.merge(left, right)`` is equalivent to ``left.join(right)``

## groupby and pivot_table
```python
DataFrame.groupby(SPLIT).OPERATION
```
SPLIT can be the following:
+ grouping keys
+ mapping index to group
+ any python function (will be applied to index)
+ combination of aboves

OPERATION can be the following:
+ column index
+ dispatch methods
+ aggregation
+ filter
+ transform 
+ apply

iteration: ``for group_index, group_obj in DataFrame.groupby(SPLIT)``.

```python
DataFrame.pivot_table(data, values=None, index=None, columns=None,
                      aggfunc='mean', fill_value=None, margins=False,
                      dropna=True, margins_name='All')
```
