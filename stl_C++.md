# STL
    <<
        The Standard Template Library (STL) is a set of C++ template classes to provide common programming data structures and functions such as lists, stacks, arrays, etc. It is a library of container classes, algorithms, and iterators. It is a generalized library and so, its components are parameterized.
    >>

# STL Sequence Containers
>>> vector
    <<
        Vectors are the same as dynamic arrays with the ability to resize itself automatically when an element is inserted or deleted, with their storage being handled automatically by the container. Vector elements are placed in contiguous storage so that they can be accessed and traversed using iterators.
    >>

>>> list
    <<
        Lists are sequence containers that allow non-contiguous memory allocation. As compared to vector, the list has slow traversal, but once a position has been found, insertion and deletion are quick.
    >>

>>> deque
    <<
        Double-ended queues are sequence containers with the feature of expansion and contraction on both ends. They are similar to vectors, but are more efficient in case of insertion and deletion of elements. Unlike vectors, contiguous storage allocation may not be guaranteed. 
    >>

# STL -> vector
    >>> declaration
    <<
        vector<int> v;
        vector<char> v;
        vector<vector<int>> v;
    >>

    >>> methods
    <<
        >> begin() - returns an iterator pointing to the first element in the vector
        >> end() - returns an iterator pointing to the theoretical element that follows the last element in the vector
        >> rbegin() - returns a reverse iterator pointing to the last element in the vector;
        >> rend() - returns a reverse iterator pointing to the theoretical element preceding the first element in the vector
        >> cbegin() - returns a constant iterator pointing to the theoretical element that follows the last element in the vector
        >> cend() - returns a constant iterator pointing to the theoretical element that follows the last element in the vector
        >> crbegin() - returns a constant reverse iterator pointing to the last element in the vector
        >> crend() - return a constant reverse iterator pointing to the theoretical element preceding the first element in the vector
    >>

    >>> element access
    <<
        >> reference operator [g] ( aka v[g]) - returns a reference to the element at position g in the vector
        >> at(g) ( almost same as v[g] ) - returns a reference to the element at position g in vector
        >> front() - returns a reference to the first element in the vector
        >> back() - returns a reference to the last element in the vector
        >> data() - returns a direct pointer to the memory array used internally by the vector to store its owned elements.
    >>

    >>> modifiers
    <<
        >> assign() - it assigns new value to the vector elements by replacing old ones ( v.assign(5, 1) fills the vector with 1 five times)
        >> push_back() - it push the elements into a vector from the back
        >> pop_back() - it is used to pop or remove elements from a vector from the back
        >> insert() - it inserts new elements before the element at the specified position
        >> erase() - it is used to remove elements from a container from the specified position or range
        >> swap() - it is used to swap the contents of one vector with another vector of the same type
        >> clear() - it is used to remove all elements of the vector container
        >> emplace() - it extends the container by inserting new element at position
        >> emplave_back() - it is used to insert a new element into the vector container, the new element is added to the end of the vector
    >>

# STL -> list
    >>> declaration
    <<
        list<int> list1;
    >>

    >>> printing the elements
    <<
        list<int>::iterator it;
        for(it = list1.begin(); it != list1.end(); ++it)
            cout << *it << " "; 
    >>

    >>> functions
    <<
        >> front() - returns the value of the first element in the list
        >> back() - returns the value of the last element in the list
        >> push_front(g) - adds new value element g at the beginning of the list
        >> push_back(g) - adds a new element g at the end of the list
        >> pop_front() - removes the first element of the list, and reduces the size of the list by 1
        >> pop_back() - removes the last element of the list, and reduces the size of the list by 1
        >> list::begin() - begin() function returns an iterator pointing to the first element of the list
        >> list::end() - end() function returns an iterator pointing to the theoretical last element which follows the last element
        >> empty() - returns whether the list is empty (1) or not (0)
        >> insert() - inserts new elements in the list before the element at a specified position
        >> erase() - removes a single element or a range of elements from the list
        >> assign() - assigns new elements to list by replacing current elements and resizes the list
        >> remove() - removes all the elements from the list, which are equal to the give element
        >> list::remove_if() - used to remove all the values from the list that correspond true to the predicate or condition given as parameter to the function
        >> reverse() - reverses the list
        >> size() - returns the number of elements in the list
        >> list_resize() - used to resize a list continer
        >> sort() - sorts the list in increasing order
        >> list_unique() - removes all duplicate consecutive elements from the list
        >> list_splice() - used to transfer elements from one list to another
        >> list_merge() - merges two lists into one
        >> list_emplace() - extends list by inserting new element at a given position
    >>

# STL -> deque
    >>> declaration
    <<
        deque<int> deque1;
    >>

    >>> printing the elements
    <<
        deque<int>::iterator it;
        for(it = deque1.begin(); it != deque1.end(); ++it)
            cout << *it << " "; 
    >>

    >>> methods
    <<
        >> deque::insert() - inserts an element
        >> deque::assign() - assign values to the same or different deque container
        >> deque::resize() - function which change the size of the deque
        >> deque::push_front() - it is used to push elements into a deque from the front
        >> deque::push_back() - this function is used to push elements into a deque from the back
    >>