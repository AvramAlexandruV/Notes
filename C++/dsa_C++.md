# Array
    <<
        Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value
    >>

    | 1 | 2 | 3 | 4 | 5 | -> the elements of the vector
      ^   ^   ^   ^   ^
      0   1   2   3   4   -> the index of the element

# String - C
    <<
        C does not have a string type, to easily create string variables create an array of characters
    >>

    | H | e | l | l | l | o | \0 | -> the elements of the vector
      ^   ^   ^   ^   ^   ^   ^
      0   1   2   3   4   5   6 -> the index of the element
    ? the \0 elements marks the end of the string 

    >>> functions
    <<
        >> strcat(char *destination, const char* source) - appends a copy of the source string to the destination string
        >> strcmp(const char * str1, const char * str2) - compares the C string str1 to the C string str2. The return value <0 ( ptr1 < ptr2 ) =0 (ptr2 = ptr1 ) >0 ( ptr1 > ptr2 )
        >> strchr(const char * str, int character) - returns a pointer to the first occurence of the character in the C string str
        >> strstr(const char * str1, const * str2) - returns a pointer to the first occurrence of str2 in str1, or a null pointer if str2 is not part of str1
        >> strtok (char * str, const char * delimiters) - a sequence of call to this function split str into tokens, which are sequences of contiguous characters separated by any of the characters that are part of delimiters
        >> strlen(const char * str) - returns the lenght of the C string str
    >>

# String - C++
    <<
        C++ has in its definition a way to represent a sequence of characters as an object of the class
    >>

    >>> declaration
    <<
        string str;
    >>

    >>> Input functions
    <<
        >> getline() - this function is used to store a stream of characters as entered by the user in the object memory
        >> push_back() - this function is used to input a character at the end of the string
        >> pop_back() - this function is used to delete the last character from the string
    >>

    >>> Capacity functions
    <<
        >> capacity() - this function returns the capacity allocated to the string, which can be egual to or more than the size of the string.
        >> resize() - this function changes the size of the string, the size can be increased or decreased.
        >> length() - this function finds the length of the string
        >> shrink_to_fit() - this function decreases the capacity of the string and makes it equal to the minimum capacity of the string.
    >>

    >>> Iterator functions
    <<
        >> begin() - this function returns an iterator to the beginning of the string
        >> end() - this function returns an iterator to the next to the end of the string
    >>

    >>> Manipulating functions
    <<
        >> copy(str, len, pos) - this function copies the substring in the target character array mentioned in its argument ( the str variable )
        >> swap() - this function swaps one string with another
    >>

# Stringstream
    <<
        Stringstream is a stream class to operate on strings. It implements input/output operations on memory (string) based streams.
    >>

    >>> operators / functions
    <<
        >> Operator ( >> ) - extracts formatted data
        >> Operator ( << ) - inserts formatted data
        >> Method str() - gets the contents of underlying string device object
        >> Method str(string) - sets the contents of underlying string device object
    >>

# Linked list
    <<
        A linked list consists of nodes where each node contains a data field and a reference to the next node in the list
    >>
    
>>> Simple linked list
    <<
        In this type of linked list, one can move or traverse the linked list in only one direction, where the next pointer of each node points to other nodes but the next pointer of the last node points to NULL.
    >>

>>> Double linked list
    <<
        In this type of linked list, one can move or traverse the list in both directions.
    >>

>>> Circular linked list
    <<
        In this type of linked list, the last node of the linked list contains the link of the first/head node of the loinked list in its next pointer.
    >>

>>> Double Circular linked list
    <<
        A double circular linked list is or circular two-way linked list is a more complex type of linked list that contains a pointers to the next as well as the previous node in the sequence.
    >>

>>> Header Linked list
    <<
        A special type of linked list that contains a header node at the beginning of the list.
    >>

# Simple linked list

# Double linked list

# Circular linked list

# Double Circular linked list

# Header Linked list

# Operatiosn with lists

# Matrix / Grid

# Stack

# Queue

# Heap

# Hash

# Graph

# Tree