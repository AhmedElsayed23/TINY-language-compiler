
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#TINY-language-compiler">TINY language compiler</a></li>
    <li><a href="#features">Features</a></li>
    <li><a href="#test-cases">Test cases</a></li>
    <li><a href="#credits">Credits</a></li>
  </ol>
</details>

# TINY language compiler
Build a compiler for TINY language in C++ that include scanner, parser, analyzer and code generator.
<p align="right">(<a href="#top">back to top</a>)</p>

## Features
* scanner
* parser
* analyzer
* code generator for evaluation
* sequence of statements separated by ;
* no procedures - no declarations
* all variables are integers
* variables are declared simply by assigning values to them :=
* if-statement: if (boolean) then [else] end
* repeat-statement: repeat until (boolean)
* for loop, and break statement: <forstmt> -> for <identifier> from <mathexpr> to <mathexpr> inc <mathexpr> startfor <stmtseq> endfor
* math expressions integers only, + - * / ^ with precedence
* I/O read write
* Comments {}
<p align="right">(<a href="#top">back to top</a>)</p>

## Test cases
You can write all the test case into input.txt file
* Test case 1 - Find power of number using for loop
  ```
  num := 1;
  read base;
  read ex;
  for i from 1 to ex inc 1
  startfor
      num := num * base
  endfor;
  write num {power}
  ```
* Test case 2 - output: 3 6 9 6 12 18 9 18 27
  ```
  for i from 1 to 3 inc 1 {nested loops, 3 loops}
  startfor
      for j from 1 to 3 inc 1
      startfor
          for k from 1 to 3 inc 1
          startfor
              if i=3 then write j*i*k end {break}
          endfor
      endfor
  endfor;
  ```
* Test case 3 - Sample program in TINY language compute factorial
  ```
  read x; {input an integer}
  if 0<x then {compute only if x>=1}
    fact:=1;
    repeat
      fact := fact * x;
      x:=x-1
    until x=0;
    write fact {output factorial}
  end
  ```
<p align="right">(<a href="#top">back to top</a>)</p>

## Credits
This project is built with my college mates and my professor Dr. Amin Allam with supervision
<p align="right">(<a href="#top">back to top</a>)</p>
