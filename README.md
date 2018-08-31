# Quicktest!

__Work in progress__

This library is based on https://www.scalacheck.org/.

Let's say you're trying to test [`strings.Join`](https://godoc.org/strings#Join). Here's how you do that:

```go
prop := Property("strings.Join")
err := prop.ForAll(func(val Val) bool {
  str := val.Get().(string)
  joined := strings.Join([]string{str, str}, "hello!")
  joined == str + "hello!" + str
})
```
