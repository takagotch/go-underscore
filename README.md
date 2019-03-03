### go-underscore
---
https://github.com/tobyhede/go-underscore

```go
var buffer bytes.Buffer

fn := func(s, i interface{}) {
  buffer.WriteString(s.(string))
}

s := []string{"a", "b", "c", "d", "e"}
Each(fn, s)

expect := "abcde"

e := un.Each(fn, s)

fmt.Printf("%#v\n", e)


var EachInt func(func(value, i int), []int)
MakeEach(&EachInt)

var sum int

fn := func(v, i int) {
  sum += v
}

i := []int{1, 2, 3, 4, 5}
EachInt(fn, i)

fmt.Printf("%#v\n", sum)



var EachStringInt func(func(key string, value int), map[string]string)
var sum int

fn := func(v int, k string) {
  sum += v
}

m := map[]int{"a": 1, "b": 2, "c": 3, "d": 4, "e": 5}
EachStringInt(fn, m)

fmt.Printf("%#v\n", sum)


Map func([]A, func(A) B) []B

s := []string{"a", "b", "c", "d"]

fn := func(s interface{}) interface{} {
  return s.(string) + "|"
}

m := un.Map(ToI(s), fn)
fmt.Println(m)

Map func ([]A, func(A) B) []B

var SMap func([]string, func(string) string) []string
un.MakeMap(&SMap)

m := un.SMap(s, fn)
fmt.Println(m)

s := []int{1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

fn := func(i interface{}) bool {
  return (i.(int) % 2) == 1
}

odd, even := un.Partition(s, fn)

fmt.Println(odd)
fmt.Println(even)


var IPartition func([]int, func(int) bool) ([]int, []int)

un.MakePartition(&IPartition)

s := []int{1, 2, 3, 4, 5, 6, 7, 8, 9, 10}

fn := func(i int) bool {
  return (i % 2) == 1
}

odd, even := un.IPartition(s, fn)

fmt.Println(odd)
fmt.Println(even)


o := "a"
s := []string{"a", "b", "c"}

b := un.Contains(s, o)
fmt.Println(b)

s := []int{1, 1, 3, 5, 8, 13}
i := un.ToI(s)
```

```
```

```
```


