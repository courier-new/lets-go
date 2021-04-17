# Let's Go! <!-- omit in toc -->

Documenting my personal journey of learning [Go](https://golang.org/).

- [About me](#about-me)
- [Why Go?](#why-go)
  - [Resources](#resources)
- [How to Start](#how-to-start)
  - [1. Introducing the language](#1-introducing-the-language)
  - [2. Trying it out](#2-trying-it-out)
    - [Setting up development environment](#setting-up-development-environment)

## About me

I think sharing context about me and my background in development is important
for framing the approach I took and correlating to what worked well and what
didn't work as well. While I hope that sharing these resources would help others
looking to get started with Go, everyone's coming from different positions, and
what worked for me certainly won't work for everyone.

- White, abled-bodied, cisgender woman from middle-class, suburban, American
  family
- Started in basic web development (HTML/CSS) in junior high and high school
- Studied physics and computer science in college
- 4 years of professional experience focused on full stack web development
  primarily in [TypeScript](https://www.typescriptlang.org/) and
  [Elixir](https://elixir-lang.org/), with significant exposure to
  [Ruby](https://www.ruby-lang.org/en/) and [Python](https://www.python.org/)

## Why Go?

I've been interested in learning Go for a while now after hearing it's more
accessible than other low-level procedural programming languages like C and C++
while still generally packing more performance than some higher-level languages
like Python or Ruby. It's also exciting to me as a more modern language than
some of those others.

Lastly, I found so much to love about Elixir, and Go aims to fit a similar set
of needs to Elixir, but having made slightly different decisions about its
design. With my limited initial understanding of Go, I see two main (practical)
differences to working with Elixir vs. working with Go:

- **Elixir** is **dynamically-typed** (technically it's "strongly-typed", but I
  found the compiler type system via Dialyzer to be slow, difficult to
  understand and trace, and unreliable), whereas **Go** is **statically-typed**
- While both languages are multi-paradigm but favoring more of a functional
  programming style, **Elixir** has stronger **functional programming**
  principals baked into it, whereas **Go** is more **object-based**: there are
  no classes or inheritance like in traditional object-oriented programming, and
  functions are defined outside of types, but Go also intentionally omits `map`,
  `reduce`, and `filter` functions from their standard library, preferring more
  explicit for loops

### Resources

- https://hackernoon.com/should-i-go-the-pros-and-cons-of-using-go-programming-language-8c1daf711e46
- https://www.cloudbees.com/blog/comparing-elixir-go/
- https://flaviocopes.com/golang-is-go-object-oriented/

## How to Start

### 1. Introducing the language

Since Go is not my first language, I wanted to start with something that would
help not just introduce the language but introduce how general programming
concepts and patterns can be applied to Go compared to other languages -- how to
write things in Go effectively. To that end, I started by reading Go's own
document, [Effective Go](https://golang.org/doc/effective_go), which "gives tips
for writing clear, idiomatic Go code" and is described as "a must read for any
new Go programmer".

### 2. Trying it out

Next up, I wanted to start getting a feel for actually working with the language
to figure out which things I could intuit and which I would need to read or
watch more about first.

#### Setting up development environment

I use [asdf](https://github.com/asdf-vm/asdf) for managing my language versions
and other command line tools, so I started by setting up
[asdf-golang](https://github.com/kennyp/asdf-golang):

```bash
$ asdf version
v0.8.0
$ asdf plugin-add golang https://github.com/kennyp/asdf-golang.git
$ asdf list-all golang
...
1.16.2
1.16.3
$ asdf install golang 1.16.3
$ asdf global golang 1.16.3
$ asdf current golang
golang          1.16.3          /Users/kelli/.tool-versions
$ go version
go version go1.16.3 darwin/amd64
```

Next comes using VSCode to write Go:

https://code.visualstudio.com/docs/languages/go