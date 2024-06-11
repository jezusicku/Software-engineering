This repository contains a series of exercises designed to practice various programming concepts using C++. The exercises cover topics such as random number generation, polynomial multiplication, quicksort algorithm, linked lists, bitwise operations, complex number arithmetic, text manipulation, file I/O, and matrix operations.

File Descriptions

Zestaw 1
This set contains implementations of several algorithms and operations.
Description: This file demonstrates various fundamental algorithms and data manipulations including:

Random number generation for array elements.
Polynomial multiplication.
Quick sort algorithm for sorting arrays.
Finding the largest number in an array.
Reversing an array.
Circular shifting of array elements.
Merging two sorted arrays.
Key Functions:

int* arrayy(int n): Generates an array of random integers.
int* mnozenie(int *arr4, int *arr5, int n, int m): Multiplies two polynomials represented as arrays.
void quick_sort(int *tab, int lewy, int prawy): Sorts an array using the quicksort algorithm.
Other utility functions to demonstrate array manipulations and algorithms.


Zestaw 2
This set implements a simple linked list.
Description: Implements basic operations on a linked list, including adding, searching, removing elements, and reversing the list.

Key Functions:

void add(Element *e): Adds an element to the list.
bool contain(const string &name): Checks if an element with a given name exists in the list.
bool isEmpty(): Checks if the list is empty.
bool remove(const string& Name): Removes an element by name.
void reverse(): Reverses the order of elements in the list.
void toarr(string arr[]): Converts the list to an array.
void removeRep(): Removes duplicate elements from the list.


Zestaw 3
This set focuses on bitwise operations.
Description: Contains functions for performing bitwise operations on unsigned short integers.

Key Functions:

unsigned short dopelnienie(unsigned short arr): Returns the bitwise complement.
unsigned short czesc_wspolna(unsigned short arr1, unsigned short arr2): Returns the bitwise AND.
unsigned short suma(unsigned short arr1, unsigned short arr2): Returns the bitwise OR.
unsigned short diff(unsigned short arr1, unsigned short arr2): Returns the bitwise difference.
unsigned short symdiff(unsigned short arr1, unsigned short arr2): Returns the symmetric difference.
bool isFound(unsigned short num, unsigned short n): Checks if a bit is set at a given position.
void add(int n): Adds a bit at a specific position.
int remove(unsigned short* set, unsigned short n): Removes a bit at a specific position.
int car(int h,int g, int c): Helper function for calculating bitwise operations.
int Cardinality(int h): Calculates the number of set bits (1s) in a number.


Zestaw 4
This set deals with complex numbers.
Description: Implements complex number arithmetic using operator overloading.

Key Functions:

Various operator overloads for +, -, *, /, ==, !=, ++, --, - (negation), and ! (conjugation).
istream &operator<<(ostream &out, const ComplexNumber &x): Overloads the << operator for complex numbers.
istream &operator>>(ostream &out, const ComplexNumber &x): Overloads the >> operator for complex numbers.



Zestaw 5
This set focuses on string and file manipulation.
Description: Includes functions for reversing text, converting numbers to words, counting zeros in a number, converting Roman numerals to integers, and reading/writing from files.

Key Functions:

void reverse(): Reads input, reverses the string, and converts to uppercase.
void read_number(int val): Reads an integer and prints its textual representation.
int count_zeros(long number): Counts the number of zero bits in a number.
void romanian(): Converts Roman numerals to integers.
void plik(): Processes a file and performs some operations.
void plik2(): Another file processing function.


Zestaw 6
This set deals with matrix operations.
Description: Implements various operations on matrices including addition, subtraction, multiplication, and transposition.

Key Functions:

void random(struct matrix *m): Fills a matrix with random numbers.
struct matrix add(struct matrix *m1, struct matrix *m2): Adds two matrices.
struct matrix sub(struct matrix *m1, struct matrix *m2): Subtracts one matrix from another.
struct matrix mult_constant(struct matrix *m, int x): Multiplies a matrix by a constant.
struct matrix mult(struct matrix *m1, struct matrix *m2): Multiplies two matrices.
void tr(struct matrix *m): Transposes a matrix.
struct matrix add_pr_diag(struct matrix *m1, struct matrix *m2): Adds primary diagonals of two matrices.
long long wyznacznik(struct matrix *m, int n): Computes the determinant of a matrix.
bool gorna(struct matrix *m): Checks if a matrix is upper triangular.
bool dolna(struct matrix *m): Checks if a matrix is lower triangular.
void print(struct matrix *m): Prints a matrix.


Zestaw 7
This set demonstrates inheritance and polymorphism with shapes and rodents.
Description: Contains class definitions and implementations for shapes (Circle, Square, Triangle) and rodents (Mouse, Gerbil, Hamster).

Key Classes and Methods:

class Shape: Abstract base class for shapes with a pure virtual draw method.
class Circle, class Square, class Triangle: Derived classes implementing the draw method.
class Rodent: Abstract base class for rodents with pure virtual name and weight methods.
class Mouse, class Gerbil, class Hamster: Derived classes implementing the name and weight methods.
How to Use
Clone the repository: git clone https://github.com/yourusername/your-repo.git
Navigate to the directory: cd your-repo
Compile the desired file using a C++ compiler, for example: g++ -o output zestaw1.cpp
Run the compiled program: ./output
Contributions
