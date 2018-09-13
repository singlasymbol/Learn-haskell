Type constructor is the name of the type and is capitalized. 

data Bool = False | True
     1        2   3  4
1. This is a type constructor.
2. Data constructor for type False.
3. | indicates the sum type. - conjunction.
4. Data constructor for type True.

Bool isn't a datatype. 

This whole thing is data declaration.

Numeric types 
- Integral Numbers
1. Int
2. Integer - Bigger Range

- Fractional
1. Float
2. Double
3. Rational
4. Scientific

Type Class is a way of adding functionality to your types that is reusable across all the types (that have instance of this typeclass).
 Num is a typeclass for which most numeric types will have an instance because there are standard functions that are convenient to have available for all types of numbers. The Num typeclass is what provides your standard (+), (-), and (*) operators along with a few others. Any type that has an instance of Num can be used with those functions. An instance defines how the functions work for that specific type. We will talk about typeclasses in much more detail soon.

Prelude> :t (/)
(/) :: Fractional a => a -> a -> a
The notation Fractional a => denotes a typeclass constraint. You can read it as “the type variable 𝑎 must implement the Fractional typeclass.”

Fractional is a typeclass that requires types to already have an instance of the Num typeclass. We describe this relationship between typeclasses by saying that Num is a superclass of Fractional. So (+) and ther functions from the Num typeclass can be used with Fractional numbers, but functions from the Fractional typeclass cannot be used with all types that have a Num instance:
