# Category Theory on Haskell

Based on https://chshersh.com/blog/2024-07-30-pragmatic-category-theory-part-01.html!

## Semigroups

From [here](https://en.wikipedia.org/wiki/Category_(mathematics)) A Semigroup isan algebraic structure consisting of a set that has this two properties:
- It is an homogenous set (a set where all the elements are of same type)
- It has one operation defined, and this operation must be associative: a x (b x c) = (a x b) x c

```haskell
module type SEMIGROUP = sig
  type t
  val x: t -> t -> t and it is associative
end

i.e:
module IntAdd = struct
  type t = int
  let append = ( + )
end

and we know that ( + ) on Real numbers is associative:
a + (b + c) = (a + b) + c
```
