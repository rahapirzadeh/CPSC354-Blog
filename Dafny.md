## Dafny Programming Language 

# Background
   Dafny is a programming language with imperative and functional features. This programming language implements reasoning in Hoare logic. Hoare logic is a formal system, or the inferring of theorems from axioms according to a set of rules, with a set of logical rules for reasoning rigorously about the correctness of computer programs. Using standard Hoare logic, only partial correctness can be proven, while termination needs to be proved separately. Dafny is a language that is designed to make it easy to write correct code. Dafny then generates a proof that the code matches the annotations. The tutorial says that this is often easier than writing the code, because annotations are shorter and more direct.
   
# Methods 
   Dafny like other imperative languages includes methods, variables, types, loops, if statements, arrays, integers, and more. In Dafny the methods is similar to a function in python but called a method because the term function has a different meaning. 
   To declare a method you state the method with a method name, and then the parameters that are taken in and their type. Then you state the returned parameters and their type. 
   ```
   method MultipleReturns(x: int, y: int) returns (more: int, less: int)
{
   more := x + y;
   less := x - y;
}
```
   In this code, when ran, the Dafny termianl lets us know that "Dafny program verifier finished with 0 verified, 0 errors
Program compiled successfully". 

   Some simple programming rules to keep in mind in Dafny is Assignments do not use "=", but rather ":=". "==" is for equality and simple statements must be followed by a semicolon and whitespace.
   
# Pre and Postconditions
   Annotations have Dafny prove the property claimed in the method is true. The two ways of an annotation are pre and post conditions. 
   Postconditions, declared with the ensures keyword, are given as part of the method's declaration, after the return values and before the method body.
   ```
   method Abs(x: int) returns (y: int)
   ensures 0 <= y
{
   ...
}
```
   Preconditions have their own keyword, requires. 
   ```
   method MultipleReturns(x: int, y: int) returns (more: int, less: int)
   requires 0 < y
   ensures less < x < more
{
   more := x + y;
   less := x - y;
}
```
   I compare postcondidtions to test functions in a way. In both lamdafun test functions were used to ensure the functions worked with different tyoes of inputs and passed the tests. Test funstions are also used in different progams such as R. 
   
# Excercise 
```
function gcd(a, b)
    while a ≠ b 
        if a > b
            a := a − b; 
        else
            b := b − a; 
    return a;
```

```
method GCD (a: int, b: int) returns (a: int)
{
  while a != b 
    invariant a == a > b
    invariant b == b > a
  {
    a := a - b;
    b := b - a;
  }
}
```
   
# Final thoughts 
   There is so much to Dafny that would be fun to work on. The syntax is a little difficult with it being very sensitive to semi colons, white space, and groupings. It is very easy to read once written however. It would be interesting to work more on Dafny for future classes. 
