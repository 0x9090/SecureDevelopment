# SecureDevelopment
Random notes on secure software development

1: Restrict all code to very simple control flow constructs. Do not use GOTO statements, setjmp or longjmp constructs, or direct or indirect recursion.

2: All loops must have a fixed upper bound. It must be trivially possible for a checking tool to statically prove that a preset upper bound on the number of iterations of a loop cannot be exceeded. If the loop-bound cannot be proven statically, the rule is considered violated.

3: Do not use dynamic memory allocation after initialization.

4: No function should be longer than what can be printed on a single sheet of paper (in a standard reference format with one line per statement and one line per declaration.) Typically, this means no more than about 60 lines of code per function.

5: The assertion density of the code should average a minimum of two assertions per function. Assertions must always be side effect-free and should be defined as Boolean tests.

6: Data objects must be declared at the smallest possible level of scope.

7: Each calling function must check non-void function return values, and the validity of parameters must be checked inside each function.

8: Preprocessor use must be limited to the inclusion of header files and simple macro definitions. Token pasting, variable argument lists (ellipses), and recursive macro calls are not allowed.

9: The use of pointers should be restricted. Specifically, no more than one level of dereferencing is allowed. Pointer dereference operations may not be hidden in macro definitions or inside typedef declarations. Function pointers are not permitted.

10: All code must be compiled, from the first day of development, with all compiler warnings enabled at the compiler’s most pedantic setting. All code must compile with these setting without any warnings. All code must be checked daily with at least one—but preferably more than one—state-of-the-art static source code analyzer, and should pass the analyses with zero warnings.
