store
=====

TBD

Example

```go
type Person struct {
	Id   string
	Name string
}

func (p *Person) Key() string {
	return p.Id
}

func main() {
	s := store.NewRedisStore()
	bob := &Person{Name: "Bob"}

	// saves to redis with a generate id
	s.Write(bob)
}
```
