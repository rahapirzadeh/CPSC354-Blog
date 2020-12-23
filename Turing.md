## Alan Turing and the Turing Machines 

# Alan Turing 
  One cannot be a couputer scientist and not know who Alan Turing is but a little background on who is and what he did. Alan was a mathematician and computer scientist, considered to be the father of theorectical computer science. I actually first learned about Alan Turing from the movie "The Imitation Game". The movie is mostly on his life and his work during WW2 working in the British intelligence agency MI6, cracking Nazi codes, including Enigma. 
  
# The Imitation Game
  The name imitation game is a term that actually comes from his paper "Computing Machinery and Intelligence," where he asks “Are there imaginable digital computers which would do well in the imitation game?” Turing then goes on to describe a game that is really a test to determine if computers can actually think. The term now called the Turing test, tests the machine's ability to exhibit intelligent beahivior equivalent to, or indistinguishable from a human.
  
  Turing's original article describes a simple party game involving three players. Player A is a man, player B is a woman and player C (who plays the role of the interrogator) is of either sex. In the imitation game, player C is unable to see either player A or player B, and can communicate with them only through written notes. By asking questions of player A and player B, player C tries to determine which of the two is the man and which is the woman. Player A's role is to trick the interrogator into making the wrong decision, while player B attempts to assist the interrogator in making the right one.If the evaluator cannot reliably tell the machine from the human, the machine is said to have passed the test.

# The Turing Machine
  The turing machine is our modern day CPU. Invented in 1936, the machine manipulated symbols on a strip of tape according to a table of rules. The machine operated on an infinite memory tape divided into discrete cells. The machine postitions its head over a cell and scans the symbol there. Then as per the symbol and the machines own present state in a finite table of user specified instructions, the machines writes a symbol in the cell, then either moves the tape one cell left or right, then as determined by the observed symbol, either proceeds to a subsequent instruction or terminates. 
  
  
# Turing Complete
  So how does this all tie to what we have been doing. I asked this exact question. Doing a little more research on the Turing Machine, the machine takes a program and shows some result, but the challenge is to have a machine read and understand many programs and run it. That is the same for programming languages. They take programs and run them. Now a programing language is called "Turing complete" if it can run any program that a Turing machine can run. Many programming languages are Turing complete because they each implement all the features required to run programs like addition, multiplication, if-else condition, return statements, ways to store/retrieve/erase data and so on. Haskell and lambdaCalculus are also turing complete.
