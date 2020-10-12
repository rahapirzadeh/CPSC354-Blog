# Lambda Calculus 

λ-calculus is a formal system in mathematical logic for expressing computation based on function abstraction and application using variable binding and substitution. The main ideas are applying a function to an argument and forming functions by abstraction. The λ calculus consists of a single transformation rule (variable substitution) and a single function definition scheme. (https://plato.stanford.edu/entries/lambda-calculus/)

I really liked λ-calculus once I saw how it was done by hand and not in code. It is a simple function, but it made it easier seeing how it was done. 

To get started, we first need to know the syntax. 
  * (λn * n + 1)0 
 
n is the variable, λn*e as the abstraction and e1, e2 is the application. 
We then apply this to all the functions. That is why λ-calculus is considered so simple. 

# Semantics of Lambda Calculus 

(λn * n + 1)0 = 0 + 1 = 1
the equal signs are considered reductions because we reason from the more compicated to the simplier side. 
Each reduction is justified by a computation rule. 
The expression that gets reduced the redex. 

When looking at the function, we see that 0 replaces n. And this is called the B rule (beta rule). 

The Beta rule: application is substitution 

### Two argument functions
In more complicated functions that take in two arguments, we have 
  * (λx * (λy * x +y))2 3
  
What this means is that whereever we have a x, we replace with 2 and whereever we have y, we replace with 3. And doing this gets rid of the λx and λy. 
  * (λx * (λy * x +y))2 3 = (λy * 2 + y) 3 = 2 + 3 = 5
  
### When an argument is a variable
  * (λx * λy * x +y)z 3
We still do the normal substitution, but we eventually have to stop. 
  * (λx * λy * x +y)z 3 = (λy * z +y)3 = z + 3
  
  In this example, x and y are the bound variables and the z and 3 are the free variables. λx and λy are binders, making sure the x and y bind. Bound Variables don't have values and are placeholders. Free variables need a value to finish the computation, to evaluate to a number. 




