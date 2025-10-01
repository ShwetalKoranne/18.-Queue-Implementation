# 18.-Queue-Implementation

Aim: To study and implement Queues in CPP.

Tools Used: VS Code or Programiz online compiler.


# Theory  
A **Queue** is a linear data structure that follows the **FIFO (First In First Out)** principle.  
- **Enqueue:** Insert an element at the rear (back).  
- **Dequeue:** Remove an element from the front.  
- **Display:** Show all elements in the queue.  

Queues are useful in scheduling, buffering, printer management, and many real-world scenarios.  

### Types of Queues  
- **Simple Queue** – basic FIFO structure.  
- **Circular Queue** – last position connects to the first.  
- **Priority Queue** – elements are dequeued based on priority.  
- **Double-Ended Queue (Deque)** – insertion and deletion at both ends.  
# Syntax
```cpp
class Queue {
    data_type arr[SIZE];   // array to store elements
    int front;             // points to front element
    int back;              // points to rear element
};
```


```

#include <iostream>
using namespace std;

class Queue {
private:
    int front, rear, size;
    int* arr;

public:
    // Constructor
    Queue(int s) {
        size = s;
        arr = new int[size];
        front = 0;
        rear = -1;
    }

    // Enqueue operation
    void enqueue(int value);

    // Dequeue operation
    void dequeue();

    // Display queue
    void display();

    // Check if queue is empty
    bool isEmpty();

    // Check if queue is full
    bool isFull();
};

```


# **Program: Queue using Array**  

### Logic:  
A `Queue` class is implemented with `enqueue()`, `dequeue()`, and `display()` functions. `front` and `back` indices track the first and last elements.Overflow occurs when the queue is full.  Underflow occurs when the queue is empty.  

### Algorithm:  
1. Start  
2. Define `Queue` class with array, front, and back.  
3. For enqueue:  
   - If full, display overflow message.  
   - Else insert element and update `back`.  
4. For dequeue:  
   - If empty, display underflow message.  
   - Else remove element and update `front`.  
5. For display:  
   - If empty, show message.  
   - Else print all elements.  
6. In `main()`, perform enqueue, dequeue, and display.  
7. End  


DETAILS:
- Define a class Queue with:
  --An integer array arr[SIZE] to store elements.
  --Two integers front and back to track the first and last elements.
- Initialize front = -1 and back = -1 in the constructor.
- Enqueue operation:
  --Check if back == SIZE - 1 → if yes, print "Queue Overflow".
  --If front == -1, set front = 0.
  --Increment back and store the value at arr[back].
- Dequeue operation:
  --Check if front == -1 or front > back → if yes, print "Queue Underflow".
  --Print arr[front] as removed element.
  --Increment front to remove the element.
- Display operation:
  --If queue is empty (front == -1 or front > back), print "Queue is empty".
  --Else, traverse from front to back and print each element.


# **Conclusion**  
Queues are important linear data structures that manage data in a **FIFO** manner. The array-based implementation demonstrates enqueue, dequeue, and display operations while handling overflow and underflow conditions. This makes queues useful in resource scheduling, buffering, and real-time applications.  
