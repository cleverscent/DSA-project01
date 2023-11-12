# DSA PROJ1

### void remove_node(struct linked_list* list, int node_location)
- remove_node() function removes a node from a linked list at the given location, checking for boundary conditions and freeing the memory.
- The function works as follows:
  - The function first checks if the list type is stack. If it is, removal is not allowed and the function returns.
  - The function then checks if the node to be removed is out of bounds. If it is, the function prints an error message and returns.
  - The function then gets a pointer to the node to be removed.
  - If the node to be removed is the head node, the function updates the head pointer and frees the memory of the node.
  - If the node to be removed is in the middle of the list, the function traverses the list to find the node, updates the pointers of the previous and next nodes, frees the memory of the node, and decrements the number of nodes in the list.
  - If the node to be removed is the last node in the list, the function updates the pointer of the previous node, frees the memory of the node, and decrements the number of nodes in the list.
  - Finally, the function checks if the list is empty. If it is, the function frees the memory of the list.

### void before_insert(struct linked_list* list, int newVal, int loc)
- before_insert() function inserts a new node with the given value before the given node in a linked list, handling all possible cases.
- The function works as follows:
  - It first checks if the linked list is empty and if the list type is normal. If either of these conditions is not met, it returns an error.
  - It then creates a new node with the given value.
  - Next, it inserts the new node before the given node, depending on the value of the location parameter.
  - Finally, it increments the number of nodes in the linked list.
    
### void search_node(struct linked_list* list, int node_value)
- The search_node() function searches for a node with the given node ID in a linked list and prints its location in the list if it is found
- It also prints a message if the node ID is not found in the list.
- The function works as follows:
  - It gets a pointer to the head node of the linked list.
  - It initializes a flag to indicate whether the node ID has been found.
  - It iterates over the linked list and compares the node ID of each node to the given node ID.
  - If the node ID is found, the function prints its location in the list and sets the flag to indicate that it has been found.
  - If the node ID is not found, the function moves to the next node in the linked list.
  - After iterating over the entire linked list, the function checks the flag to see if the node ID was found. If it was not found, the function prints a message indicating so.
  - Finally, the function frees the memory allocated for the target node pointer.

### void convert_to_circularLinkedList(struct linked_list* list)
- The convert_to_circularLinkedList() function converts a singly linked list to a circular linked list by updating the next and prev pointers of the head and tail nodes of the linked list.
- The function works as follows:
  - It checks the list type to make sure it is normal. If it is not, the function prints an error message and returns.
  - It updates the next pointer of the tail node to point to the head node. This makes the linked list a closed loop.
  - It updates the previous pointer of the head node to point to the tail node. This makes the linked list doubly linked.
  - It sets the list type to 2 to indicate that the linked list is now circular.
  - It prints a message to the console indicating that the conversion is complete.

### void rotate_circularLinkedList(struct linked_list* list, int rotate_num)
- The rotate_circularLinkedList() function rotates a circular linked list by the given number of times by updating the head and tail pointers of the linked list.
- The function works as follows:
  - It checks the list type to make sure it is circular. If it is not, the function prints an error message and returns.
  - It iterates over the linked list for the given number of times.
  - For each iteration, the function updates the head and tail pointers of the linked list to point to the next node in the linked list.
  - After iterating over the linked list, the function prints a message to the console indicating that the rotation is complete.

### int check_empty(struct Stack* stack)
- The function checks if the top pointer of the stack is pointing to a valid node.
- If it is not, then the stack is empty and the function returns 1.
- Otherwise, the stack is not empty and the function returns 0.
### int check_full(struct Stack* stack)
- The function checks if the top pointer of the stack is pointing to the last index of the stack array.
- If it is, then the stack is full and the function returns 1.
- Otherwise, the stack is not full and the function returns 0.
### int push(struct Stack* stack, int item)
- The function first checks if the stack is full by calling the check_full() function.
- If it is, the function prints an error message and returns -1.
- Otherwise, the function increments the top pointer of the stack and adds the given item to the stack at the index pointed to by the top pointer.
- Finally, the function returns 1 to indicate success.
### int pop(struct Stack* stack)
- The function first checks if the stack is empty by calling the check_empty() function.
- If it is, the function prints an error message and returns -1.
- Otherwise, the function retrieves the top item of the stack by dereferencing the top pointer, decrements the top pointer, and returns the popped item.
### int peek(struct Stack* stack)
- The function first checks if the stack is empty by calling the check_empty() function.
- If it is, the function prints a message indicating that the stack is empty and returns -1.
- Otherwise, the function retrieves the top item of the stack by dereferencing the top pointer and returns it.
### int perform_operation(int operand_1, int operand_2, char operator)
- The function takes two operands and an operator as input and returns the result of performing the operation on the operands.
- The function uses a switch statement to handle the different operators.
- If the operator is +, -, or *, the function performs the corresponding operation on the operands and returns the result.
- If the operator is /, the function checks if the second operand is 0.
- If it is, the function prints an error message and returns -1.
- Otherwise, the function performs the division operation and returns the result.
- If the operator is invalid, the function prints an error message and returns -1.
### int compute_postfix_expression(const char* expression)
- compute_postfix_expression() function computes the value of a postfix expression by using a stack to store the operands.
- The function works as follows:
  - It creates a stack.
  - It iterates over the expression character by character.
  - If the character is a digit, it converts it to an integer and pushes it onto the stack.
  - If the character is a space, it ignores it.
  - If the character is an operator, it pops the top two operands from the stack, performs the operation on them, and pushes the result onto the stack.
  - If the character is invalid, it prints an error message and returns -1.
  - After iterating over the entire expression, it checks if there is only one element left on the stack.
  - If there is, it pops the element from the stack and returns it as the result.
  - Otherwise, it prints an error message and returns -1.
