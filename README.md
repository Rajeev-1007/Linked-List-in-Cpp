# Linked-List-in-Cpp
# Name: Rajeev Ramesh Reddy E
# PRN: 24070123081

Aim: To implement and understand the concept of singly linked lists in C++ through node creation, traversal, and insertion operations.

Software Used: Vs Code.

Theory: 

Singly linked lists in C++ are dynamic data structures composed of nodes, where each node contains data and a pointer to the next node. They allow efficient memory usage and flexible insertion or deletion without shifting elements. Implementing them involves creating a `Node` class, linking nodes via pointers, and traversing the list using loops or recursion. Operations like insertion at the beginning, end, or specific position help reinforce pointer manipulation and foundational understanding of linked data structures.

Syntax:

    #include <iostream>
    using namespace std;

    // Node structure
    struct Node {
    int data;
    Node* next;
    };

    // Function to insert at the end
    void insertEnd(Node*& head, int value) {
    Node* newNode = new Node{value, nullptr};
    if (head == nullptr) {
        head = newNode;
        return;
    }
    Node* temp = head;
    while (temp->next != nullptr) {
        temp = temp->next;
    }
    temp->next = newNode;
    }

    // Function to traverse and display the list
    void display(Node* head) {
    Node* temp = head;
    while (temp != nullptr) {
        cout << temp->data << " -> ";
        temp = temp->next;
    }
    cout << "NULL" << endl;
    }

    int main() {
    Node* head = nullptr;

    insertEnd(head, 10);
    insertEnd(head, 20);
    insertEnd(head, 30);

    cout << "Linked List: ";
    display(head);

    return 0;
    }


Algorithm:

i) Algorithm: Node Creation in Singly Linked List (C++)

 1. Define Node Class
- Create a class `Node` with two members:
  - `int val` to store data.
  - `Node* next` to point to the next node.

 2. Constructor Initialization
- Define a constructor that:
  - Assigns the input `data` to `val`.
  - Sets `next = NULL` to indicate the end of the list.

 3. Create Node in `main()`
- Instantiate a new node `n` using `new Node(20)`.

 4. Display Node Data
- Print the value and pointer of the node using `cout`.

 5. End Program
- Return 0 to indicate successful execution.

ii) Algorithm: Singly Linked List with Head Insertion (C++)

 1. Define Node Class
- Create a class `Link` with:
  - `int data` to store the node's value.
  - `Link* next` to point to the next node.
- Initialize these in the constructor.

 2. Insert at Head
- Define `insert_head(Link*& head, int data)`:
  - Create a new node with the given data.
  - Set its `next` to the current `head`.
  - Update `head` to point to the new node.

 3. Display Function
- Define `disp(Link* head)`:
  - Traverse the list using a temporary pointer.
  - Print each node’s data followed by `" --> "` until reaching `NULL`.

 4. Main Execution
- Initialize `head` as `NULL`.
- Call `insert_head()` multiple times to add nodes at the beginning.
- Call `disp()` after each insertion to show the current list.

 5. End Program
- Return 0 to indicate successful execution.

iii) Algorithm: Singly Linked List Traversal in C++

 1. Define Node Class
- Create a class `Node` with:
  - `int val` to store the node's value.
  - `Node* next` to point to the next node.
- Initialize these in the constructor.

 2. Create Nodes
- Dynamically allocate three nodes (`n1`, `n2`, `n3`) with values 10, 20, and 30 respectively.

 3. Link Nodes
- Set `n1->next = n2` and `n2->next = n3` to form the linked list: `10 → 20 → 30 → NULL`.

 4. Traverse List
- Use a temporary pointer `temp` starting at `n1`.
- Loop through the list while `temp != NULL`, printing each node’s value.

 5. End Program
- Return 0 to indicate successful execution.

Conclusion:

Singly linked lists in C++ offer a foundational understanding of dynamic data structures and pointer manipulation. Through node creation, traversal, and insertion, learners grasp how data can be efficiently organized and modified in memory. Mastering these operations builds confidence in handling more complex structures like stacks, queues, and trees, reinforcing core programming logic.
