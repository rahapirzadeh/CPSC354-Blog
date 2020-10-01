# Haskell: Recursion in Functional Programming
To start, I downloaded [Haskell](https://www.haskell.org/platform/) for my Mac OS.
Haskell is a functional programming language which I had never used before. Functional programming means that the program treats computation as the evaluation of mathematical functions and avoids changing state and mutable data.
To get started on learning Haskell, I found this [online tutorial](http://tryhaskell.org/). The tutorial taught me the basics of Haskell and what it can do, such as

```Haskell
sort[44,21,33,2]
```
or 
```Haskell
let add1 x = x + 1 in add1 5
```
Haskell has very short and clear code. 

##### To further learning Haskell, I wrote the following functions for the homework assignment...
```Haskell
revert [] = []
revert (x:xs) = revert xs ++ [x]

member n [] = False
member n (x:xs)
 | n == x = True
 | otherwise = member n xs

append :: [a] -> [a] -> [a]
append [] ys = ys
append (x:xs) ys = x : (append xs ys)

select_odds (x:xs) = x:select_evens xs
select_odds [] = []

select_evens (_:xs) =select_odds xs
select_evens _ = []

less_equal:: [Int] -> [Int] -> Bool
less_equal xs ys = if xs >= [] && ys <= [] then
   True
 else 
   False
   
select_odd [] = []
select_odd[x] = [x]
select_odd(y:x:xs) = y:select_odd(xs)

select_even[] = []
select_even[x] = []
select_even(y:x:xs) = x:select_even(xs)
```
The assignment was not too hard. I did have to look into online tutorials and online blogs to get comfotable with the syntax. By not learning Haskell first, I assumed the programs to be longer and not as simple as they were when i was done with them. 

### Similarites
I have seen some similarites between Haskell and Python. 
```python
a=[1,4,2,44]
a.sort()
print(a)
```
```Haskell
sort[44,21,33,2]
```
While Haskell is purely functional, Pyton is a mix of procedual, object oriented and functional. 
Both have similar syntax, however Haskell is much more condensed, leading to shorter lead times.  

