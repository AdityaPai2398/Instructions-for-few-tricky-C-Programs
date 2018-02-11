# Instructions-for-few-tricky-C-Programs
Some decriptions to keep in mind while analysing crypto/trick c programs

1) Else without a previous if
   Use flower brackets; there can't be a block of code that is not contained in an if befoe an else.
   
2) #define and precedence
   Be careful when replacing the preprocessor don't forget about the rules of precedence.
   
3) Switch takes only  integer and characters
   As characters are integers in ascii format
   
4) For loop with a semi colon at the end of it does not execute the statements within it's block.

5) Else if is true for integers except 0 (even negative numbers work).

6) Duplicate case values not allowed

7) #ifdef INDIA 
       //block of code 
   #endif 
   This block of code is executed only if Macro Named India is defined.This is called as conditional execution
   
8) void ( *ptr[3])();  //array of pointer to a function that return void
   Brackets are important or else it means that the function is returning a void pointer
   ptr[0]=one; //yes! it's just like that no need of any brackets
   ptr[1]=two;
   //now to call a function named "two"
   ptr[1]();    //this calles a function named two it's similar to "two()"
   
9) char p[]="%d";
   creates p[0]='%' p[1]='d' p[2]=\0
   p[1]='c'; // replaces d with c;
   printf(p,65); //equivalent to printf("%c",65); output is A //ascci 65 is A
   
10)Cannot access address of a variable which is a register.
   
