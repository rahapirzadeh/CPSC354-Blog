# Parse Trees
Parsing is a process of analyzing a string of symbols in a computer language, conforming to the grammer rules. I like comparing parsing to the elementary school method of PEMDAS. There is a set order to which the operation muct be done in and parsing is the way a computer program solves equations. 

Parsing is putting the parenthesis where they need to go. Lets say we have 1*2*3*4. This is simple because you just multiply all the numbers together and it can be in any order. 
   * ((1*2)*3)*4)
   * (1*2)*(3*4)
   * (1*(2*3))*4
   * 1*((2*3)*4)
   * 1*(2*(3*4))
   
Now lets say we have 1+2*3. There is only one way which we can put the parentheis that the equation will be solved correctly. 
   * 1+(2*3)
   
This is all written in the rules. 
``` Haskell
Plus. Exp ::= Exp "+" Exp1 ;
Num. Exp2 ::= Integer ;
Times. Exp1 ::= Exp1 "*" Exp2 ;
```
The rule is telling us that for multiplication, we take the integer to the right of the sign and to the left. Then we go to to the addition sign and do the same. 
