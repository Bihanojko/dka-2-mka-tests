# dka-2-mka-tests
A testing script and a set of tests for dka-2-mka project

Extract into the same folder as Makefile and necessary source files. The script compares actual 
and reference outputs on the basis of plain file comparison, so it is suggested you adjust the
reference output files to match your state naming conventions.

#### Conventions currently in use
Input automaton is made complete by adding sink state if neccessary. Sink state is assigned least number from [0,1..] not yet in use.

Rules in output are sorted as whole strings (for example 1,a,2 is "1,a,2") in ascending lexicographic order (e. g. 1,a,2 < 1324,a,2 < 2,a,2). To use numeric sorting convetion use optional -numeric argument (see Usage). Numeric sorting uses rule componets separatedly with priority (from most important to least importrant): current state, input symbol, next state (e. g. 1,a,2 < 1,b,1 < 1234,a,1)

#### Usage
$ python3 dka-2-mka-test.py [-numeric]

-numeric: use numeric sorting convetion

Another set of useful tests can be found at https://github.com/vokracko/FLP-DKA-2-MKA-test
