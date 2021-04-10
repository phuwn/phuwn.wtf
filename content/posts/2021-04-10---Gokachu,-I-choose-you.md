---
title: Gokachu, I choose you!
date: "2021-04-10T00:00:00.000Z"
template: "post"
draft: false
slug: "gokachu-i-choose-you"
category: "Technology"
tags:
  - "Thoughts"
  - "Go"
  - "Language"
  - "Golang"
  - "Technology"
description: "A brief description about my first and favorite Pokémon in the stack, Go"
socialImage: "/media/post_4_img_1.jpeg"
---

As a trainer, I’ve teamed up with a lot of Pokemons throughout my entire short career. Some bring me the power to build masterpieces, some give me an unpleasant partnership. But after all, I do cherish the time we spent together. Today I want to share my thoughts about my favorite of them all, my right-hand Pokemon, Go (or Golang).

![SonGolang (From the internet)](/media/post_4_img_1.jpeg)

## What is Go?

Go is a programming language that

- Is created by Google
- Is simple
- Has lightning-quick compile speed
- Makes sharing code easy
- Utilizes the power of multi-cores & concurrency mechanism
- Carries the beauty of system programming along with the modern language feature

## Skills

#### 1. Simplicity in Type System

So how simple is Go? Go is an open-source programming language that makes it easy to build software while still holds cool stuff like code reuse, reliability, concurrency, low-level systems accessibility, … It provides a type system that motivates you to code with joy, not some high architecture headache.

- Go has efficient reference types like slices, hashmap, string, … that provide good resource managing while you have no worry.
- Go implements type embedding that helps you focus on code reuse instead of drawing confusing inheritance hierarchy.
- Go allows you to implement Interfaces through only the set of behavior. It’s called duck typing — if it quacks like a duck, then it can be a duck. This lets you simply write your methods without going through a list of implementation that's longer than your family tree.

![Clearly a Duck.. is Typing](/media/post_4_img_2.jpeg)

#### 2. Lightning-Quick Compile Speed

Dynamic languages provide quick productivity but the trade-off is they don’t offer the type safety that static languages do and often need a comprehensive test suite to avoid discovering incorrect type bugs at runtime. On the other hand, Static languages like C ensure the workflow logic but often provide slow compile speed. Go is here to solve the case. Here are some of Go powers to boost the speed:

- `gofmt` is a tool that automatically formats your source code and checks for syntax errors without actually building the project. This could reduce the number of imperfect builds.
- Go has a special library tree that makes dependency analysis easy. When it comes to compile-time, Go ‘s package manager only has to look up in the `$GOROOT` and `$GOPATH` directory, it follows exactly the path you provide. So this could save a lot of time from the package finding process.
- The language has been designed to be easy to analyze and can be parsed without a symbol table.

![Programmer Excusing for legitimately slacking of "My Code's Compiling."](/media/post_4_img_3.png)

#### 3. Support the Power of Open Source

The evolution of the digital age has changed the way we build our programs. We don’t have to code every single piece of our app anymore, we make use of functions, services from another team in the company, or maybe a third-party library, or even from just some guys on the internet that come up with a solution for our issue. The power of code sharing has become more important than ever before. And that’s one of the reasons that Go is created for.

- After you publish your code, any developers that want to reuse your code just have to pull it to their local and put it under the Go library tree. And then walah, your code helps the world. Cool right?
- Go even has godoc, a tool for package documentation. Having troubles using some package? Search for in on godoc mai fen.

![Import my own package easy-peasy](/media/post_4_img_4.png)

#### 4. Utilizes the power of multi-cores and concurrency mechanism

No doubt, Concurrency has been the coolest feature of Go since one of its core creators is Rob Pike, the man who built concurrency languages more than thirty years ago. Now, Go is famous for its power in concurrency. There’re articles about Go and its [Concurrency vs Parallelism](https://blog.golang.org/waza-talk) all over the internet. But the truth is Go does support both of them. It makes use of the power of multi-cores effectively while still adapts the concurrency mechanism. And its power in concurrency doesn’t just stop there. Everyone knows that threads are lightweight processes. But Go’s logic doesn’t run on threads, it has its own implementation called goroutines, lightweight threads.

- Goroutines are spawned from the OS thread. They exist only in the virtual space of Go runtime and only under control of Go runtime, not OS.
- They have a faster startup time than threads and can be created with only **2 KB** stack size while Java thread takes about **1 MB** stack size.
- With a single logical processor, hundreds of thousands of goroutines can be scheduled to run concurrently with amazing efficiency and performance.
- When it comes to multithreading, there’s always some complicated stuff comes along like shared resource and race condition. Go Concurrency implements the CSP model, a message-passing model that works by communicating data between goroutines instead of locking data to synchronize access. Data is passed through Go channels, and Go runtime will decide which Goroutines run and hold the resource in the meantime. You could focus only on logic handling instead of multithread headaches.

![Concurrency vs Parallelism](/media/post_4_img_5.jpeg)

#### 5. System Programming Ability

The language is designed to be productive but still holds the power of system programming. Since Go code is compiled to machine code, it has the lightning speed and low-level programming accessibility of a low-level system language (like C/C++) however, it also provides you with some of the convenience of higher-level system languages like garbage collection and the power of run-time reflection.

- The standard library provides all the core packages that give us the power of lower-level programming (dealing with implementation details of the machine, like pointers, network protocols, files, process, …)
- Go’s garbage collection adds little overhead to program execution time but reduces development effort significantly. You don’t have to manage your resource memory manually, Go’s garbage collector will assassinate it for you.
- Go Runtime Reflection will smartly handle your data without your notice about its existence.

## Use cases

Go has been widely used as a modern replacement for C/C++ in all kinds of areas. But I personally think that Go has its own purpose, its best usage is for microservices, web servers, and network-based systems since it provides reliability, fast, and network handling ability. Here are a few use cases and supported tools:

- Microservices system: Go kit, Micro, Gizmo, Kite, Goa, Caddy, …
- REST API Server: Gin, Martini, Revel, Gorilla, Beego, …
- RPC API Server: gRPC, Twirp, Spiral, Gorilla
- GraphQL API Server: graphql-go, gqlgen, Thunder
- WebAssembly: Hugo, Vugu, TinyGo, Vecty
- Robotics, IoT & Embedding Programming: Gobot, Mainflux, TinyGo, EMBD
- CLI application: Cobra, cli
- AI, Machine Learning: GoLearn, Gorgonia
- Blockchain development
- Mobile application: gomobile
- Desktop application: Lorca, Wails, Fyne
- Game application: Ebiten, Pixel, G3N

## Reference

- [Go In Action —William Kennedy (Book)](https://www.oreilly.com/library/view/go-in-action/9781617291784/)
- [What makes Go so Difference](https://betterprogramming.pub/what-makes-go-so-different-eb0648498ce0)
- [Concurrency and Channels in Go](https://medium.com/trendyol-tech/concurrency-and-channels-in-go-bbc4dea75286)
- [Concurrency vs Parallelism](https://blog.golang.org/waza-talk)
- [How does the Go language compile so fast compared to Java](https://www.quora.com/How-does-the-Go-language-compile-so-fast-compared-to-Java)
- [Reflection in Go](https://www.integralist.co.uk/posts/reflection-in-go/)

---

Thank you for hearing my thoughts about Go. Due to my lack of experience, the article may contain some inaccurate information. Please inform me if you found any.

[My post on Medium](https://phuwn.medium.com/gokachu-i-choose-you-efd4da2603c1). Would you care for giving me a clap? Thank you :D
