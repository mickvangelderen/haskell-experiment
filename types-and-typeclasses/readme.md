# Summary

 * In `ghci`, `:t <expression>` shows you the type of `<expression>`. 
 * `::` means "has a type of".
 * A list has a readable type representation: `:t "Hello"` gives `[Char]`. 
 * A tuple also has a nice representation: `:t (True, 1)` gives `(Bool, Int)`. 
 * `String` is synonymous to `[Char]`.
 * `Int` represents a whole number. It has a min- and maximum value. 
 * `Integer` represents a big number. Useful in RSA algorithms and such which deal with enormous numbers. Obviously is less performant than `Int`.
 * `Float` can represent a fractional number.
 * `Double` is a `Float` with double the precision.
 * `Bool` is either `True` or `False`.
 * `Char` represents a single character.
 * `()` is the type of the empty tuple `()`.
 * `:t head` gives `[a] -> a` where `a` is a "type variable". A type variable can be replaced by any type (unless constrained to a typeclass).
 * To use an infix function as a prefix function, use parenthesis: `(==)`.
 * `:t (==)` gives `Eq a => a -> a -> Bool`. `Eq` is a typeclass and basically requires whatever the type variable `a` will be replaced with to implement the `Eq` interface.
 * `=>` separates the class constraints from the argument types.
 * `Eq` members implement `(==)` and `(/=)`. 
 * `Ord` members implement `(<)`, `(<=)`, `(>)` and `(>=)`. An `Ord` member is also an `Eq` member. because `a == b` is equivalent to `a >= b && a <= b` and `a /= b` is equivalent to `a < b || a > b`. 
 * `compare :: Ord a => a -> a -> Ordering` does what you expect it to and returns an Ordering.
 * `Ordering` is either `LT`, `EQ` or `GT`.
 * `Show` members can be represented as a `String`. I think they implement `show :: Show a => a -> String`.
 * `Read` members can be read from a `String`. I think they implement `read :: Read a => String -> a`.
 * You can specify the expected type of an expression: `read "5" :: Int`. 
 * `Enum` members can be enumerated. They can therefore be used in list ranges. They also have predefined successors and predecessors, retrieved with `succ :: Enum a => a -> a` and `pred :: Enum a => a -> a`. Members of this class are:
    * `Bool`
    * `Char`
    * `Ordering`
    * `Int`
    * `Integer`
    * `Float`
    * `Double`
 * `Bounded` members have a minimum and maximum value retrieved with `minBound :: Bounded a => a` and `maxBound :: Bounded a => a`.
 * Tuples of which all members are `Bounded` are also `Bounded` themselves.
 * `Num` members are able to act like numbers. `Int`, `Integer`, `Float` and `Double` are members.
 * `Integral` members are whole numbers.
 * `Floating` members are fractional numbers.
 * `fromIntegral :: (Integral a, Num b) => a -> b`
