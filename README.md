Hi Gophers! Unfortunately, I don't have the time to maintain this library right now, so I can't add any features. I'll gladly accept pull requests if you're interested. Also, if you'd like to maintaining the library longer term, I'm also happy to welcome you as a contributor. If you're interested in either submitting a PR or being a longer term maintainer, please let me know on the [Gophers Slack](https://invite.slack.golangbridge.org/). My username there is `arschles`.

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
