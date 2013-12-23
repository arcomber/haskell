haskell
=======

Programming in Haskell by Graham Hutton exercises

I started from chapter 4.  Thought earlier exercises too basic to bother with publishing.

To feel a bit like a diary I have noted where I faltered or made a wrong decision to show the decision making process in getting to a final solution.

This book is an excellent introduction to Haskell.  Yes there are some very good free online resources such as LYAH, and I did start there but I didn't like just reading.  I wanted to be exercised along the way to check my understanding.  This book has exercises at the end of each section which so far seem set at the right sort of level.  They may require a little thought and time in places but generally most readers should be able to come up with some sort of an answer.

One point to note is the book uses the n + k concept which has been dumped now because it is deemed not really necessary and can cause confusion.

n + k is this:

drop :: Int -> [a] -> [a]
drop 0 xs     = xs
drop (n + 1) []     = []
drop (n + 1) (_:xs) = drop n xs 

But it is pretty pointless and you can easily convert to this:

drop :: Int -> [a] -> [a]
drop 0 xs     = xs
drop n []     = []
drop n (_:xs) = drop (n - 1) xs 

So don't get too hung up about that.  You can mentally convert as per example above.

Apart from that tiny issue (which is fair enough because at the time it was probably seen as a useful feature) the book is excellent as a first step into learning the language.
