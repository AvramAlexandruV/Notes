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
    >>> node structure
    <<
        struct Node {
            int data;
            struct Node* next;
        }
    >>

    >>> main
    <<
        struct Node* head = NULL;
        struct Node* second = NULL;
        struct Node* third = NULL;

        head = (struct Node*)malloc(sizeof(struct Node));
        second = (struct Node*)malloc(sizeof(struct Node));
        third = (struct Node*)malloc(sizeof(struct Node));

        head->data = 1; head->next = second;
        second->data = 2; second->next = third;
        third->data = 3; third->next = NULL;
    >>
>
    >>> traversal
    <<
        void traversal(struct Node* n){
            while(n != NULL){
                cout << n->data << " ";
                n = n->next;
            }
        }
    >>
>
    >>> add node at the front ( O(1) )

    1) allocate node
    2) put in the data
    3) make next of new node as head
    4) move the head to point to the new node

    <<
        void front(struct Node** head_ref, int new_data){
            //1
            struct Node* new_node = (struct *Node)malloc(sizeof(struct Node));

            //2
            new_node->data = new_data;
            
            //3
            new_node->next = (*head_ref);
            
            //4
            (*head_ref) = new_node;
        }
    >>
>
    >>> add node after given node ( O(1) )

    1) check if the given node is NULL
    2) allocate new node
    3) put in the data
    4) make next of new node as next of prev_node
    5) move the next of the prev_node as new_node

    <<
        void given(struct Node* prev_node, int new_data){
            //1
            if(prev_node == NULL){
                return;
            }

            //2
            struct Node* new_node = (struct Node*)mallloc(sizeof(struct Node));

            //3
            new_node->data = new_data;

            //4
            new_node-next = prev_node->next;

            //5
            prev_node->next = new_node;

        }
    >>
>
    >>> add node at the end ( O(1) )

    1) allocate node
    2) put in the data
    3) this new node is the last, make next of it nulll
    4) if the linked list in empty, then make the new node as head
    5) else traverse till the last node
    6) change the next of last node

    <<
        void end(struct Node** head_ref, int new_data){
            //1
            struct Node* new_node = (struct Node*)malloc(sizeof(struct Node));

            struct Node *last = *head_ref;

            //2
            new_node->data = new_data;

            //3
            new_node->next = NULL;

            //4
            if(*head_ref == NULL){
                *head_ref = new_node; return;
            }

            //5
            while(last->next != NULL)
                last = last->next;

            //6
            last->next = new_node;
        }
    >>
>
    >>> delete from beginning
    
    1) point head to the second node

    <<
        head = head->next;
    >>

    >>> delete from end

    1) traverse to second last element
    2) change its next pointer to null

    <<
        struct Node* tmp = head;
        while(tmp->next->next != NULL){
            tmp = tmp->next;
        }
        tmp->next = NULL;
    >>
>
    >>> delete from middle
    
    1) traverse to element before the element to be deleted
    2) change next pointers to exclude the node from the chain

    <<
        for(int i = 2; i < pos; i++){
            if(tmp->next != NULL){
                tmp = tmp->next;
            }
        }

        tmp->next = tmp->next->next;
    >>
>
    >>> search an element

    1) make head as the current node
    2) run a loop till the node is nul
    3) each iteration check for the value

    <<
        bool search(struct Node** head_ref, int val){
            struct Node* current = *head_ref;

            while(current != NULL){
                if(current->data == val) return true;
                current = current->next;
            }
            return false;
        }
    >>
>
    >>> sort

    1) make head as the current node and create another node index for later use
    2) if head is null, return
    3) else, run a loop till the last node
    4) in each iteration do steps 5 and 6
    5) store the next node of current in index
    6) check if the data of the current node is greater than the next node. If it is greater, swap current and index

    <<
        void sortLinkedList(struct Node** head_ref) {
            struct Node *current = *head_ref, *index = NULL;
            int temp;

            if (head_ref == NULL) {
                return;
            } else {
    
            while (current != NULL) {
                index = current->next;

  	            while (index != NULL) {
                    if (current->data > index->data) {
                        temp = current->data;
                        current->data = index->data;
                        index->data = temp;
    	            }
    	        index = index->next;
  	            }
  	        current = current->next;
                }
            }
        }
    >>

# Matrix / Grid

# Stack

# Queue

# Heap

# Hash

# Graph

# Tree