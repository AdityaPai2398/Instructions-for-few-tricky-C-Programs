# Instructions-for-few-tricky-C-Programs
Some descriptions to keep in mind while analysing crypto/tricky c programs

1) Else without a previous if
   Use flower brackets; there can't be a block of code that is not contained in an if befoe an else.
   
2) #define and precedence
   Be careful when replacing the preprocessor don't forget about the rules of precedence.
   
3) Switch takes only  integer and characters
   As characters are integers in ascii format
   
4) For loop with a semi colon at the end of it does not execute the statements within it's block.It executes only wgen condition no longer holds good.

5) Else if is true for all integers except 0 (even negative numbers work).

6) Duplicate case values not allowed in switch statemebts 

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

11)A structure variable can be assigned to other using =, but cannot be compared with other using ==

12)A structure cannot contain a member of its own type because if this is allowed then it becomes impossible for compiler to know size of such struct. Although a pointer of same type can be a member because pointers of all types are of same size and compiler can calculate size of struct

13)Memory allocated for the union is equal to memory needed for the largest member of it, and all members share this same memory space.

14)In C, struct and union types cannot have static members. In C++, struct types are allowed to have static members, but union cannot have static members in C++ also.

15)Deep copies are more expensive, due to needing to create additional objects, and can be substantially more complicated, due to references possibly forming a complicated graph.

16)What is designated Initialization?
Designated Initialization allows structure members to be initialized in any order. This feature has been added in C99 standard.
struct Point p2 = {.x = 20}; This feature is not available in C++ and works only in C.
