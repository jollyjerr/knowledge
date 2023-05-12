# SQL

Not an overview but here are some hot tips:

Select a table twice to make comparisons

```SQL
select one.id from Weather one, Weather two 
where dateDiff(one.recordDate, two.recordDate) = 1 
and one.temperature > two.temperature;
```
