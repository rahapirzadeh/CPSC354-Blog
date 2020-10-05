# Assignment 1: Part 2

For assignment 1 part 2, we had to implement a calculator and we were able to use the built-in Haskell functions. This way is much more efficient since we are using binary numbers instead of suceesor numbers. 

An interpreter for abstract syntax
   * file(s) numbers3.hs 


An interpreter for concrete syntax
   * file(s) Interpreter.hs numbers.cf Calculator.hs
    
    
In this part I countered several technical difficulties. I found this [BNFC tutorial](https://bnfc.digitalgrammars.com/tutorial/bnfc-tutorial.html)
that helped me understand what I was doing and to install BNFC. 
I am using a mac, so I first used homebrew to install BNFC.
```
brew install bnfc
```
After I installed BNFC I ran 
```
bnfc -m --haskell numbers.cf
``` 
And that generated a list of new files. However, not all the files compiled, and I had a error that I need Alex to compile one of the files. Using several different online methods on installing Alex, I finally was successful with 
``` 
brew install cabal-install
cabal install alex
cabal install happy
```
These lines allowed me to compile the rest of the files.
```
bnfc -m --haskell numbers.cf
alex LexNumbers.x
make
echo "1+2*3" | ./TestNumbers
```
The echo line is used once everything is compiled and a parser test executable is created. 

BNFC or BNF Converter is the standard format for the specification and documentation of programming languages. BNFC can be used in projects in C, C++, C#, Haskell and even Java. It’s very useful when designing and implementing new programming languages. In Haskell, the three tools needed to have installed are
   * GHC - Haskell compiler
   * Alex - a lexer generator for Haskell
   * Happy - a parser generator for Haskell


In a BNFC file, you will find a sequence of rules to help with parsing in a tree. The parse rules tell the program how to solve the problem and the order. Parsing is all about putting the parenthesis in the right place. The more rules you have, the lower number of trees you can make.


As i found out in my research, BNFC is used in other programming languages too. The others I'm familiar with are C++ and java. In particular, in Java, the syntax is a little different. 
``` 
bnfc -m -java1.5 numbers.cf
make
```
Once compiled, to run the parser test class, you run
```
echo "23 + 4 * 70" | java numbers/Test
```
Now, BNFC is a little more complicated in Java than in Haskell, eventhough Haskell has more rough corners. Like in Haskell, you need a parser and lexer, called Cup and JLex. Finally, you need to sett the Java class path. 

Just from looking at one of the files, the main class, you can see several of the similarites. Both languages use their lexer and parser to print the parser tree. The java class looks more simplified and by changes the tree output to a call of the interpreter. In haskell, the string is first lexed and parsed. 



An interpreter in Java: main class

``` Java
  public class Interpret {
      public static void main(String args[]) throws Exception
      {
        Yylex l  = new Yylex(System.in) ;
        parser p = new parser(l) ;
        Calc.Absyn.Exp parse_tree = p.pExp() ;
        System.out.println(Interpreter.interpret(parse_tree)) ;
      }
    }
```
An interpreter in Haskell: the main function
``` Haskell
module Main where

import LexNumbers
import ParNumbers
import AbsNumbers
import Interpreter

import ErrM
import PrintNumbers

main = do
  interact calc
  putStrLn ""

calc s =
  let Ok e = pExp (myLexer s)
  in printTree (eval e)
 ```
