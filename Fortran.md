## Fortran

# What is Fortran 
  Fortran is a compiled imperative programming language that is used for numeric computations and scientific computing. It was developed in the 1950's and although it is rarely used today, giant simulations of the type that run for days on the world’s most massive supercomputers, are most likely Fortran code. While structured programming, object orientation, functional programming, and logic programming all arose to solve various problems that supposedly were not solved by primitive Fortran, none of the languages that embodied these new organizing principles came close to supplanting Fortran in the realm for which it was invented: scientific and numerical computing. 
  
# Who is replacing Fortran
  Now this is where things get interesting. Of the three young languages with the potential to move beyond Fortran is Haskell. While Fortran is part of Turing machine branch of the language world, Haskell is under the lambda calculus branch, making it Turing complete but also these programs are conceived as the composition of functions rather than as a series of explicit steps.

  While Fortran provides a comfortable translation of mathematical formulas, Haskell code begins to resemble mathematics itself. With its elaborate type system and pattern matching, the beginnings of function definitions in Haskell look like the setups of proofs in mathematical monographs, with definitions and axioms carefully established.
  
  Lets use fib as our example. 
  ```
  fib :: Integer -> Integer
  fib 0 = 1
  fib 1 = 1
  fib n = fib (n-1) + fib (n-2)
  ```
  The code is simple to read and looks straight out of the textbook. Its purely functional nature allows programs to be constructed with a high degree of confidence in their correctness and it's due to Haskell’s sophisticated type system.
  
  In Fortran, since you cannot have recursion, you cannot write easy to write and uunderstandable programs. For example, factorial in Fortan is like this...
  ```
  function fact(n)
  integer fact, n, p
  p = 1
  do i = 1, n
  p = p * i
  end do
  fact = p
  end
  ``` 
  while in Haskell it is much more straightforward and looks like a formula. 
  ```
  fac n
	| n == 1    = 1
	| otherwise = fac (n - 1) * n
  ```
  
# Final thoughts 
  While fortran was very impressive for the time, there are better and fater programming languages that do what Fortran does in a cleaner and simpler way. I only touched on Haskell as that is what we learned in this class, but another language to look at is Julia. 
  
  
