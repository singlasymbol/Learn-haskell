Types - Types are way of categorizing values.

String - list of characters

ghci

Prelude> :type 'a'
'a' :: Char 

Single quotes tell the compiler that it is a character not a variable.
:: says the 'has the type'- Whenever you see this in haskell, it means, you are reading a <b>'type signature'</b>

Char is the type that contains alphabetic characters, unicode characters, symbols etc.

Prelude> :type "Hello!"
"Hello!" :: [Char]

[] is a syntatic sugar for a list.

String is a <b><i>type alias </i><b> for a list of Char.

Ways to print in haskell

print "Haskell!"
Prelude> "Haskell!" -- with the quotes

putStrLn "hello world!"
Prelude> hello world!

putStr "hello world!"
hello world!Prelude>

<!-- module Print1 where -->
<!-- main :: String -> IO() -->
<!-- main str = putStrLn str -->

Here, main has type IO. It stands for input/output.

<!-- main :: IO()
main = do
    putStrLn "Hello"
    putStrLn "World!"
    putStrLn "hello hello"
    putStrLn "world world!" -->

The do syntax allows the sequencing the actions.

Concatenate Strings- 
Types

Prelude> :t (++)
(++) :: [a] -> [a] -> [a]

Prelude> :t concat
concat :: Foldable t => t [a] -> [a]

(++) :: [a] -> [a] -> [a]

Everything after the :: is about our types, not our values. The ‘a’
inside the list type constructor [] is a type variable.
1. Take an argument of type [a]. This type is a list of elements of some type 𝑎. This function does not know what type 𝑎 is. It doesn’t need to know. In the context of the program, the type of 𝑎 will be known and made concrete at some point.
2. Take another argument of type [a], a list of elements whose type we don’t know. Because the variables are the same, they must be the same type throughout (a == a).
3. Return a result of type [a]


The type variable 𝑎 in [a] is polymorphic. Polymorphism is an important feature of Haskell. For concatenation, every list must be the same type of list