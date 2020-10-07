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
Precedence is how the tree parses the numbers. Exp has precedence 0, Exp1 has precedence 1 and Exp2 has precedence 2. So for Plus, its saying to form an expression of level 0 from an expression of level 0 on the left of + and of level 1 on the right. The same goes for Times, form an expression of level 1 from an expression of level 1 on the left of * and of level 2 on the right.
