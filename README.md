# University Database

This project provides users with a range of functionality within a university database. The program allows users to: 
* Input and manage student and faculty data
* Delete records
* Display information
* Update a student's advisor by providing the student's ID along with the new faculty ID
* Remove an advisee from a faculty member using their respective IDs

This is accomplished through Binary Search Trees and List Stacks. Every student is associated with one faculty member as their advisor, and every advisor has a list of student(s) as their advisees. Identifying information about the students and advisors are stored as nodes. The program saves the last instance of the Trees/Menu (student and faculty) when the program closes successfully. The next time the program runs, it reads from the studentTable and facultyTable files and rebuilds the trees with the same information. 

## Identifying Information

* Name: Ryan King
* Email: Ryanhking9@gmail.com
* Course: CPSC 350 - Data Structures
* Date: Fall 2021
* Assignment: University Database

## Source Files

* Faculty.cpp
* FileProcessor.cpp
* Menu.cpp
* Student.cpp
* main.cpp

## References

* Used GeeksForGeeks to figure out how to get depth of Node
* Used GeeksForGeeks to help with implementation of scapegoat tree
* Used stackoverflow.com for help with appending data to file

## Known Errors

* None

## Example Input and Output 

* Example student and faculty tables for running the program given in runLog.txt.

## Build Instructions

* <code> g++ -o test.o *.cpp </code>

## Execution Instructions

* <code> ./test.o </code>
* The order that FileProcessor reads the file to make the tree is in FileProcessor process file methods. Example of this order is given in facultyTable.txt and studentTable.txt. To start from no file, remove those files first. 
* IDs cannot be -1. The program assumes that the ID will never be equal to -1, so we use it to check that a student/faculty member does not exist in the table. 
* When adding a new faculty member, you cannot give it a student ID that does not exist in the student table (you can, it just doesn't do anything). If you give a student ID that does not exist, it will create the faculty member but it will not include that student ID in the advisee list and it will not create a new student in student table with that ID.
