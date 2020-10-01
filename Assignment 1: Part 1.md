# Assignment 1: Part 1

For assignment 1 we had to use recursion over algebraic data types. This assignment was a little confusing for me in the beginning. 
I went to office hours that that helped me understand the logic behind the functions. 
Once I became used to the data types, the assignment went smoothly. 
The first part included functions in

  * Natural numbers
  * Postive numbers
  * Fractions
  
To be honest, I did not see the point of Haskell untill I finished the assignment. For each function, you had to simplify it and think critically. It slightly made me a better programmer to think of the algorithms to solve the problems. 

For example, lets take the simple function of addition. When you think abput it, you instantly want to say it's just a number added to another number. But how do you code that "add" in Haskell? Since Haskell uses recursion, you simply use the function. And just like other coding languages, you have to make sure you have all the cases covered. In Haskell, if cases overlap, the program process from top to bottom. 

```Haskell
add :: NN -> NN -> NN
add O n = n                   
add (S n) m = S (add n m)  
```
To understand this function, you have to see the type being inputed and the type being returned. In this case, we have a natural number and are being returned a natural number. The first case we have to think about is 0. Any number added to 0 is just the number. We also defined the natural number data type of O to equal 0. The third line is what tripped me up. We know that the next case is a number added to another and we need to initerate through that. In the original data type we declared S as a function 1 that basically means its being iterated, hence, S (add n m). 

Once I thought I understood that portion, I had to do about positive numbers, that dont include 0, meaning the base case is 1.

```Haskell
addP :: PN -> PN -> PN
addP I n = T n
addP (T n) m = T (addP n m) 
```
Here we have a positive number inputed and a positive number being outputted. Since we can't have a zero, we have to make the case for it. For positive number data types, we defined that I = 1 and T is the function. 

My favorite functions were the fractions. It truely was like a puzzle, especially when converting the types and figuring out the simplest way do the function and with the functions we already have done. 
