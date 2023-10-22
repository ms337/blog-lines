---
layout: page
title: Implementing Scheme in Haskell
category: devproject
---

Functional programming, Scheme, Haskell, Compiler Theory, Basic Category Theory

In this project, I implement a Scheme interpreter comprising a parser and an evaluator in Haskell. The parser type is a monad and this allows the construction of the total Scheme parser as a composition of simpler parsers. For the evaluator, I use monads to handle side-effects and scoping throughout the evaluation of S-expressions. The implementation includes a standard library of functions, and basic macros that make the language capable of modifying its own syntax.

[Repository](https://github.com/ms337/SchemeInHaskell)
