### Hi there 👋

```go
	if _, e := eg.SQL("SELECT current_database()").Get(&name); e != nil {
		err = fmt.Errorf("failed to get database name: %w", e)
		return
	}
	if _, e := eg.SQL("SELECT version()").Get(&version); e != nil {
		err = fmt.Errorf("failed to get database version: %w", e)
		return
	}
	return name, version, nil
```
