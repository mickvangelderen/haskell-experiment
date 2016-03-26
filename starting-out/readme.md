# Summary

 * In `ghci`, `:set prompt "something "` changes the prompt to `something `.
 * `+`, `-`, `*`, `/` work as expected.
 * `&&`, `||`, work as expected, `not` for boolean negation. 
 * To fix "cannot mix infix", use parenthesis to specify what you wa `5*(-3)`.
 * Operators are actually functions.
 * Prefix function: `func arg1 arg2`, example: `add 1 2`.
 * Infix function: `arg1 func arg2`, example: `1 + 2`.
 * Equality: `==`.
 * Inequality: `/=`.
 * Function is defined by `func arg1 arg2 ...`, no parenthesis or commas.
 * Function arity seems to define the meaning of `a b c d`, it could mean `a(b, c)(d)`, `a(b)(c, d)` or `a(b)(c)(d)` depending on the definition `a`, `b`, `c`, and `d`. (Not sure if correct)
 * A binary function can be called as infix by surrounding the funct name with backticks: `div 9 2` is the same as `9 ``div`` 2`.
 * There is only a ternary if written as `if x then y else z`.
 * There are no variables, only constants/aliases/definitions/names. When you define `thing = "This is a thing."`: `thing` and `"This a thing."` are exactly the same thing. 
 * An apostrophe `'` is a valid function name character.
 * Function names cannot start with an uppercase letter.
 * In `ghci`, use `let <definition>` to define something. 
 * `[1, 2, 3]` denotes a list with elements 1, 2 and 3.
 * The elements of a list must all be of the same type.
 * Strings are lists of characters.
 * `a ++ b` concatenates lists `a` and `b`.
 * `a : l` prepends an element `a` to the list `l`.
 * `l !! i` takes element `i` from list `l`.
 * Lists can be compared (from low to high indices) if their elements can be compared. 
 * `head l` returns the first element of list `l`.
 * `tail l` returns all but the first element of list `l`.
 * `last l` returns the last element of list `l`.
 * `init l` returns all but the last element of list `l`.
 * `length l` returns the length of list `l`.
 * `null l` returns whether or not list `l` is empty.
 * `reverse l` returns list `l` in reverse.
 * `take n l` returns the first `min(length l, n)` elements of `l`.
 * `drop n l` returns all but this first `min(length l, n)` elements of `l`.
 * `minimum l` returns the smallest element in list `l`. Elements must be orderable.
 * `maximum l` returns the largest element in list `l`. Elements must be orderable.
 * `sum l` returns the sum of all elements in list `l`.
 * `product l` returns the product of all elements in list `l`.
 * `elem e l` returns whether or not element `e` is a in list `l`. 
 * Ranges allow you to create lists: `[1, 3 .. 10]` returns `[1, 3, 5, 7, 9]`. `[0.1, 0.3 .. 1]` returns `[0.1,0.3,0.5,0.7,0.8999999999999999,1.0999999999999999]` which is extremely weird to me because `1.0999` > `1`.
 * Infinite range: `take 5 [1, 3 ..]` returns `[1, 3, 5, 7, 9]`, the first 5 elements of the infinite sequence `1 + 3n (n >= 0)`. 
 * `cycle l` repeats list `l` infinitely.
 * `repeat e` is `cycle [e]`.
 * `replicate n e` is `take n (repeat e)`.
 * `[x - 1 | x <- [1, 4, 10]]` is a list comprehension and outputs `[0, 3, 9]`.
 * List comprehensions have the following form: `[ <output> | <input>, ..., <predicate>, ... ]`
 * Tuples are unnamed data structures: `(a, b, ...)` where `a` and `b` may be of any type. 
 * A tuple has its own type based on its element's. 
 * `fst (a, b)` returns `a`.
 * `snd (a, b)` returns `b`.
 * `zip [1, 2] ['a', 'b']` returns `[(1, 'a'), (2, 'b')]`.
 * `zip [1] ['a', 'b', 'c']` returns as much as possible `[(1, 'a')]`.

