# Haskell

## What I learned for greater good

- <i class="fa fa-user"></i>&nbsp;Christoph Welcz
- <i class="fa fa-calendar" aria-hidden="true"></i>&nbsp;18.04.2018
- <i class="fa fa-twitter" aria-hidden="true"></i>&nbsp;[@ChristophWelcz](https://twitter.com/ChristophWelcz)
- <i class="fa fa-github" aria-hidden="true"></i>&nbsp;[github.com/enolive/haskell-intro](https://github.com/enolive/haskell-intro)

<--->

## Why Haskell?

![funx-flagellation](resources/Striding_flagellant.jpg)

Note: Source [Wikipedia](https://en.wikipedia.org/wiki/Self-flagellation)

<-->

- force myself to use FP
- leave my comfort zone
- undestand libraries like [Ramda](http://ramdajs.com/) or [Vavr](http://www.vavr.io/).

<--->

<!-- .slide: data-background-image="resources/fp-club.png" -->

<--->

![noborder-haskell logo](resources/haskell-logo.png)

- Pure functional language
- Static typed
- First version 1990
- For mathematicians
- GHC (Glasgow Haskell Compiler)

<--->

<section tagcloud large>
First Class Functions
Infix
Function Composition
Guards
Pattern Matching
List Comprehensions
Lazy/Strict Evaluation
Partial Application
(Un-)Currying
Eta Conversion
(Un-)Folding
Crazy Stuff 
</section>

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