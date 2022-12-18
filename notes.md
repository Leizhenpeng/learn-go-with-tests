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
## slice

1. 切片和数组的声明方式
```
mySlice := []int{1,2,3} 而不是 mySlice := [3]int{1,2,3}
```

2. 可变参数 `...`
```go
func SumAllTails(numbersToSum ...[]int) (sums []int) {

	for _, numbers := range numbersToSum {
		if len(numbers) == 0 {
			sums = append(sums, 0)
		} else {
			tail := numbers[1:]
			sums = append(sums, Sum(tail))
		}
	}

	return sums
}
```
