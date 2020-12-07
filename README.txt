# OS_ex1
// OS- semester A- class B2 
// ID 315566810 login:- barif 
// ID 311593313 login:- sharonlevi 
// ex3
//Date - December 7th, 2020
********************************************************************************** 
ALL PROGRAMS ARE EXECUTED VIA UNIX TERMINAL ALL PROGRAMS COMPILED VIA TERMINAL- USING COMMAND "gcc -Wall (filename.cc) -o (runfilename) 
Programs are executed via terminal. './<runFileName>.
**********************************************************************************
//in this program we set a 50K size array, filled with random numbers, between 0 to 200K.
//now we give birth to 2 childs, one that performs a binary search, the other- serial search.
// we go trough a loop 1000 times now:
// the father proccess sends a number in the given range through Pipe.
// every child looks for the wanted number in the way it was built(BS, S-s)
// each child will return to std output how much time it took to find the number.
// after 1000 runs in loop, father will send -1 to childs and kills them
// output will be- 
// bs avg time, ss avg time,bs min time, ss min time, bs max time, ss max time
// mention- srand seed will be 17.
********************************************************************************** 
//in this program we set a 50K size array, filled with random numbers, between 0 to 200K.
//now we give birth to 2 childs, one that performs a binary search, the other- serial search.
//Each child in an infinite loop: takes a random number and send to the father along with the 
//child's ID through the father's pipe. The father checks if the number is in his array, 
//then deletes it from the array. The father sends the child, on a designated pipe of the child, an answer 
//as to whether the number he sent did/ not caused a deletion of value in the father.
//When the father finishes emptying the array he kills the children by sending the signal SIGTERM
//The father shows how long it took him to complete the task. How many numbers he got, and how many he deleted
