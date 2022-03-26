+++
title = "Studying: Structure and Interpretation of Computer Programs"
description = "23/??? Amazing Eva is organizing a book club"
date = 2022-03-08
draft = false
slug = "first-book-club"

[taxonomies]
categories = ["journal"]
tags = ["learning", "lisp", "community"]

[extra]
comments = true
+++

Programs conjure processes.

Lisp languages call processes "procedures".

It blurs the idea between passive data and active process, making it a good language to write programs that must manipulater other programs as data (such as interpreters and compilers).

There are two kinds of elements in programming: procedures and data.

Omg, what a catastroph. Lisp implements some weird kind of RPN, but not really. Code like `(+ 10 12 12)` is valid. It's a tree structure eval. I think it's the same for every data thing on Clojure at least, according to Nick.

Declaring vars `define var 2`.

The general form of a procedure definition is:

```
(define (<name> <formal parameteres>) <body>)

#e.g

(define (square x) (* x x))
```

This is the ugliest square function definition I ever saw in my entire life.

I don't really understand (or care) for the difference between *normal-order eval* and *applicative-order eval*, should I?
Seems like I should cause it's gonna be used later on.

Ifs:

```
(define (abs x)
    (cond ((> x 0) x)
          ((= x 0) 0)
          ((< x 0) (-x))))
```

It's basically an `if`, `if else`, `if else`.

You can also:

```
(define (abs x)
    (cond ((< x 0) (-x))
    (else x)))
```

Or:

```
(define (abs x)
    (if (< x 0)
        (-x)
        x))
```

You can use `and`, `or`, `not`...

Processes are generated by procedures. A procedure is a pattern for the local evolution of a computational process. 

Here's an example of factorial function:

```
(define (factorial n)
(if (= n 1)
    1
    (* n (factorial (- n 1)))))
```

I'll stop mentioning how ugly everything looks as this will get in the way of me learning this.

Just had a cool insight, about the shape of the outputs of functions!
Big O notation is just a mathematical expression of their shapes. Kinda cool.

Should we code the example on page 40? Should I? Probably?
I wonder if that's how you create a map...

Seems like the example on page 50 might offer some interesting insights on Big O, but I don't feel like it right now8

- I don't really understand for loops.