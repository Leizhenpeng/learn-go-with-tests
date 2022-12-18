# Learn Go with Tests

## Hello word

1. `t.Errorf`

```go
 t.Errorf("got %q want %q", got, want)`
```



2. `t.heper()`

```go
  assertCorrectMessage := func(t *testing.T, got, want string) {
        t.Helper()
        if got != want {
            t.Errorf("got %q want %q", got, want)
        }
    }
```

