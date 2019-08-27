
# Tuples

## Defining Tuples

* Tuples are dumb containers
* Perfect for grouping items
* Perfect for returning two items or three or four particularly if they are different types

## Creating a Tuple


```scala
val ta = (1, "cool", 402.00)
val tb:(Int, String, Double) = (1, "cool", 402.00)
val tc:Tuple3[Int, String, Double] = (1, "cool", 402.00)
```


    Intitializing Scala interpreter ...



    Spark Web UI available at http://32c6e00c8fb3:4042
    SparkContext available as 'sc' (version = 2.4.3, master = local[*], app id = local-1562173222978)
    SparkSession available as 'spark'
    





    ta: (Int, String, Double) = (1,cool,402.0)
    tb: (Int, String, Double) = (1,cool,402.0)
    tc: (Int, String, Double) = (1,cool,402.0)
    



There is a `Tuple1`, `Tuple2`, `Tuple3`,…​`Tuple22`

## Getting the values from a Tuple


```scala
val ta = (1, "cool", 402.00)
println(ta._1)
println(ta._2)
println(ta._3)
```

    1
    cool
    402.0
    




    ta: (Int, String, Double) = (1,cool,402.0)
    



The _1, _2 comes from Haskell’s first and second functions

## Swapping Tuple

Only a `Tuple2` can be swapped


```scala
val t2 = ("Foo", 40.00)
println(t2.swap) //(40.00, "Foo")
```

    (40.0,Foo)
    




    t2: (String, Double) = (Foo,40.0)
    



### Syntactic Sugar for Tuples

* `Tuple2` can also be created with `→` (dash-arrow)
* The `→` is a method that is on every object that accepts another object
* If you're curious, the `→` is an implicit wrapper defined in `scala.Predef` 


```scala
val t2 = "Foo" -> 40.00 // (40.00, "Foo")
```




    t2: (String, Double) = (Foo,40.0)
    



**Tip:** You can use the `-` and `>` or you can use the unicode rightwards arrow: `→`

## Conclusion

* Tuples are just dummy containers, they just hold stuff.
* Tuples are typed
* There are tuples that go all the way to Tuple22
* Tuple2 has swap
* Tuples are immutable, become an essential part not only in the Scala language, but functional programming as well.
