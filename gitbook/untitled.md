# Rest API with GO

This is why you are here. Or I hope this is why you are here.

{% embed url="https://talks.golang.org/2012/splash.article" %}

This above article came out in 2012. But still pretty relevant to learn the ideology behind go.

If you are writing Rest API why should you choose go?

1. It's compiled. So you get small binaries.
2. It's fast. \(slower than c/c++ or rust\) but faster than most other web programming languages.
3. It's simple to understand.
4. It works really well in the microservices world for reason no 1.

### net/http

The standard library in go comes with the `net/http` package, which is an excellent starting point for building RestAPIs. And most other libraries the adds some additional feature are also interoperable with the net/http package so understanding the net/http package is crucial to using golang for RestAPIs.

{% embed url="https://golang.org/pkg/net/http" %}

We probably don't need to know everything in the net/http package. But there are a few things we should know to get started.

### The Handler Interface

I am never a proposer of memorizing something but as [Todd Mcleod](https://twitter.com/Todd_McLeod) in his course mentions over and over. We need to memorize the Handler interface.

```text
type Handler interface {
        ServeHTTP(ResponseWriter, *Request)
}
```

And here it is. 

It has one method and one method only.

A struct or object will be Handler if it has one method `ServeHTTP` which takes `ResponseWriter` and pointer to `Request`. 



With all our knowledge now we are ready to do some damage.

