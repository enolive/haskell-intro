# What I learned by learning Haskell 

- <i class="fa fa-user"></i>&nbsp;Christoph Welcz
- <i class="fa fa-calendar" aria-hidden="true"></i>&nbsp;03.05.2018
- <i class="fa fa-twitter" aria-hidden="true"></i>&nbsp;[@ChristophWelcz](https://twitter.com/ChristophWelcz)
- <i class="fa fa-github" aria-hidden="true"></i>&nbsp;[github.com/enolive/haskell-intro](https://github.com/enolive/haskell-intro)

<--->

## Why Haskell?

<-->

<!-- .slide: class="outline" "data-background-image="resources/Striding_flagellant.jpg" -->

Note: Source [Wikipedia](https://en.wikipedia.org/wiki/Self-flagellation)

<-->

- force myself to use FP
- leave my comfort zone
- understand libraries like [Ramda](http://ramdajs.com/) or [Vavr](http://www.vavr.io/).

<--->

<!-- .slide: data-background-image="resources/fp-club.png" -->

Note: Source [Fight Club](https://en.wikipedia.org/wiki/Fight_Club)

<--->

![noborder-haskell logo](resources/haskell-logo.png)

- Pure functional language
- Statically typed
- First version 1990
- For mathematicians

<-->

|Tool|Description|
|---|---|
|GHC|**G**lasgow **H**askell **C**ompiler|
|GHCi|GHC interactive, aka REPL|
|Stack|project templates, dependency management, build|
|Hoogle|documentation database|
|HSpec|write and run tests with a BDD syntax similar to RSpec|
|HLint|the linter, d'oh!|

<--->

<section tagcloud large>
First Class Functions
Infix Syntax
Recursion
Function Composition
Guards
Pattern Matching
List Comprehensions
Lazy/Strict Evaluation
Partial Application
(Un-)Currying
Eta Conversion
(Un-)Folding
Zipping
Functors
Maybe
Either
Crazy Stuff 😉
</section>

<--->

## Haskell Stack Commands

```bash
# creates a new project using the default template
stack new my-project name
# starts the REPL
stack ghci
# starts the local hoogle documentation server
stack hoogle server
# runs all tests
stack test
```

<--->

## Important GHCi Commands

|Command|Meaning|
|---|---|
|:r|Reloads all modules|
|:t TYPE|Shows type information|
|:m MODULE|loads the given module (public-only)|
|:m *MODULE|loads the given module (all)|
|:l FILE|loads the given file into the module|

<--->

## Hello World

```haskell
module HelloWorld
    ( greet
    ) where

greet :: String -> String
greet name = "Hello, " ++ name ++ "!"
```

<--->

## Factorial

```haskell
fac :: Int -> Int
fac 1 = 1
fac n = n * fac (n - 1)
```

<--->

## Fibonacci Sequence

```haskell
-- see also 
-- https://stackoverflow.com/questions/1105765/generating-fibonacci-numbers-in-haskell
fibs :: [Int]
fibs = 1 : 1 : zipWith (+) fibs (tail fibs)

fib :: Int -> Int
fib n = fibs !! n
```

<--->

## Useful stuff

- [Haskell Stack](https://docs.haskellstack.org/en/stable/README/)
- [IntelliJ-Haskell](https://github.com/rikvdkleij/intellij-haskell)
- [Hoogle](https://www.haskell.org/hoogle/)
- [Learn You a Haskell for Great Good!](http://learnyouahaskell.com/)
- [Exercism Haskell Track](http://exercism.io/languages/haskell)