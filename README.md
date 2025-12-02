# Settings
automatically searches for vedau.toml settings applied in this order: vedau.toml, run-time set

- df
- frontend
- metrics

# Logic

```python
v(*args, **kwargs) 
```

- `v()` - prints info about current df if set
- `v(**kwargs)` - set settings
- `v(df)` - prints info about  df and sets it as working df
- `v(df, **kwargs)` - if it is first call, set settings from kwargs
- `v(s: pd.Series)` - plot pd series
- `v(df, string)` - searchs for `string` in df.columns and plots as pd.Series
- `v(s1: pd.Series, s2: pd.Series)` - treats as y_pred and y_true, compares them, prints mertics (if set)
