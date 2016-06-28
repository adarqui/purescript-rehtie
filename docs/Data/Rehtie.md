## Module Data.Rehtie

#### `rehtie`

``` purescript
rehtie :: forall a b c. Either a b -> (a -> c) -> (b -> c) -> c
```

Takes an `Either` value and two functions, if the value is a `Left` the
inner value is applied to the first function, if the value is a `Right`
the inner value is applied to the second function.

``` purescript
rehtie (Left x) f g == f x
rehtie (Right y) f g == g y
```


