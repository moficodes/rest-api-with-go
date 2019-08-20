# API

If you have been around a computer for long enough you probably heard of this thing. What is this API?

API stands for Application Program Interface. Like most thing in computer science the abbreviation doesn't help much.

What it actually means is it exposes functionality without exposing internals. If you program in a language that supports writing functions or methods \(pretty much all programming languages\)  you would totally understand what I am talking about. 

```text
func addNumber(a, b int) int {
    // DO AMAZING MATH HERE
    // and return the result
}
```

Even if you are super new to go, you can tell this function is about adding two numbers and returning the result. 

For the user of the function you just call the function and never worry about how the function is doing what it does \(don't trust every function\). 

Thats all an API is. An API could be a function you wrote, or a function from a library or method from a framework, or a http endpoint.

