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


## integer
1. run `go test` will auto test it

```
func ExampleAdd() {
	sum := Add(1, 5)
	fmt.Println(sum)
	// Output: 6
}
```

## iteration
1. `go test -bench=.`

```
func BenchmarkRepeat(b *testing.B) {
    for i := 0; i < b.N; i++ {
        Repeat("a")
    }
}
```
