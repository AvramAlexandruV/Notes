# STL
    <<
        The Standard Template Library (STL) is a set of C++ template classes to provide common programming data structures and functions such as lists, stacks, arrays, etc. It is a library of container classes, algorithms, and iterators. It is a generalized library and so, its components are parameterized.
    >>

# STL Algorithms
>
    >>> Sorting
    <<
        sort(start_address, end_address);
    >>
>
    >>> Searching
    <<
        binary_search(start_address, end_address, value_to_find);
        ? returns true or false
    >>
>
    >>> Non-Manipulating Algorithms
    <<
        >> sort(first_iterator, last_iterator) - to sort the given vector
        >> sort(first_iterator, last_iterator, greater<int>()) - to sort the given container/vector in descending order
        >> reverse(first_iterator, last_iterator) - to reverse a vector
        >> *max_element(first_iterator, last_iterator) - to find the maximum element of a vector
        >> *min_element(first_iterator, last_iterator) - to find the minimum element of a vector
        >> accumulate(first_iterator, last_iterator, initial value of sum) - does the summation of vector elements
        >> count(first_iterator, last_iterator, x) - to count the occurences of x in vector
        >> find(first_iterator, last_iterator, x) - returns an iterator to the first occurrence of x in vector and points to last address of vector, if element is not present in vector
        >> binary_search(first_iterator, last_iterator, x) - test wether x exists in sortef vector or not
        >> lower_bound(first_iterator, last_iterator, x) - returns an iterator pointing to the first element in the range [first,last) which has value not less than 'x'
        >> upper_bound(first_iterator, last_iterator, x) - returns an iterator pointing to the first element in the range [first,last) which has a value greater than 'x'
    >>
>
    >>> Manipulating Algorithms
    <<
        >> arr.erase(position_to_be_deleted) - this erases selected element in vector and shifts and resizes the vector elements accordingly
        >> arr.erase(unique(arr.begin(),arr.end()),arr.end()) - this erases the duplicate occurences in sorted vector in a single line
        >> next_permutation(first_iterator, last_iterator) - this modified the vector to its next permutation
        >> prev_permutation(first_iterator, last_iterator) - this modified the vector to its previous permutation
        >> distance(first_iterator, desired_position) - it returns the distance of desired position from the first iterator.
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
>
    >>> declaration
    <<
        vector<int> v;
        vector<char> v;
        vector<vector<int>> v;
    >>
>
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
>
    >>> element access
    <<
        >> reference operator [g] ( aka v[g]) - returns a reference to the element at position g in the vector
        >> at(g) ( almost same as v[g] ) - returns a reference to the element at position g in vector
        >> front() - returns a reference to the first element in the vector
        >> back() - returns a reference to the last element in the vector
        >> data() - returns a direct pointer to the memory array used internally by the vector to store its owned elements.
    >>
>
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
>
    >>> declaration
    <<
        list<int> list1;
    >>
>
    >>> printing the elements
    <<
        list<int>::iterator it;
        for(it = list1.begin(); it != list1.end(); ++it)
            cout << *it << " "; 
    >>
>
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
>
    >>> declaration
    <<
        deque<int> deque1;
    >>
>
    >>> printing the elements
    <<
        deque<int>::iterator it;
        for(it = deque1.begin(); it != deque1.end(); ++it)
            cout << *it << " "; 
    >>
>
    >>> methods
    <<
        >> deque::insert() - inserts an element
        >> deque::assign() - assign values to the same or different deque container
        >> deque::resize() - function which change the size of the deque
        >> deque::push_front() - it is used to push elements into a deque from the front
        >> deque::push_back() - this function is used to push elements into a deque from the back
    >>

# STL Container Adaptors
>>> queue
    <<
        Queues are a type of container adaptors that operate in a first in first out (FIFO) type of arrangement. Elements are inserted at the back (end) and are deleted from the front. Queues use an encapsulated object of deque or list (sequential container class) as its underlying container, providing a specific set of member functions to access its elements.
    >>

>>> stack
    <<
        Stacks are a type of container adaptors with LIFO(Last In First Out) type of working, where a new element is added at one end (top) and an element is removed from that end only.  Stack uses an encapsulated object of either vector or deque (by default) or list (sequential container class) as its underlying container, providing a specific set of member functions to access its elements.
    >>

# STL -> queue
>
    >>> declaration
    <<
        queue<int> queue1;
    >>
>
    >>> printing the elements
    <<
       while(!queue1.empty()){
            cout << queue1.front() << " ";
            queue1.pop(); 
       }
    >>
>
    >>> methods ( O(1) complexity )
    <<
        >> queue::empty() - returns whether the queue is empty
        >> queue::size() - returns the size of the queue
        >> queue::swap() - exchange the contents of two queues
        >> queue::emplace() - insert a new element into the queue container, the new element is added at the end of the queue
        >> queue::front() - returns a reference to the first element of the queue
        >> queue::back() - returns a reference to the last element of the queue
        >> queue::push(g) - adds the element g at the end of the queue
        >> queue::pop() - deletes the first element of the queue
    >>

# STL -> stack
>
    >>> declaration
    <<
        stack<int> stack1;
    >>
>
    >>> functions ( O(1) complexity )
    <<
        >> empty() - returns wether the stack is empty
        >> size() - returns the size of the stack
        >> top() - returns a reference to the top most element of the stack
        >> push(g) - adds the element g at the top of the stack
        >> pop() - deletes the top most element of the stack
    >>

# STL Associative Containers
>>> set
    <<
         Sets are a type of associative container in which each element has to be unique because the value of the element identifies it. The values are stored in a specific sorted order i.e. either ascending or descending.
    >>

>>> map
    <<
        Maps are associative containers that store elements in a mapped fashion. Each element has a key value and a mapped value. No two mapped values can have the same key values.
    >>

# STL -> set
>
    >>> declaration
    <<
        set<int> s;
    >>
>
    >>> functions
    <<
        >> begin() - returns an iterator to the first element in the set
        >> end() - returns an iterator to the theoretical element that follows the last element in the set
        >> size() - returns the number of elements in the set
        >> max_size() - returns the maximum number of elements that the set can hold
        >> empty() - returns wether the set is empty
        >> count(const g) - returns 1 or 0 if the element g is present in the set or not
        >> erase(const g) - removes the value g from the set
        >> clear() - removes all the elements from the set
    >>

# STL -> map
>
    >>> declaration
    <<
        map<string,int> map1;
    >>
>
    >>> printing the elements
    <<
        map<string,int>::iterator it = map.begin();
        
        while(it != map.end()){
            cout << "Key" << it->first << "Value" << it->second;
            ++it;
        }
    >>
>
    >>> functions
    <<
        >> begin() - returns an iterator to the first element in the map
        >> end() - returns an iterator to the theoretical element that follows the las element in the map
        >> size() - returns the number of elements in the map
        >> max_size() - returns the maximum number of elements that the map can hold
        >> empty() - returns wether the map is empty
        >> pair_insert(key_value, map_value) - adds a new element to the map
        >> erase(iterator_position) - removes the element at the position pointed by the iterator
        >> erase(const g) - removes the key-value g from the map
        >> clear() - removes all the elements from the map
    >>