## Simple Implementation of Priority Queue (Delete Function Only)

## Aim:
To implement the delete operation in a Priority Queue, where elements with the highest priority (lowest numerical value) are removed first.

## Procedure:

1.A priority queue is represented using a list of tuples, where each tuple contains:

  * The data (string or number).
  
  * Its priority (integer).

2.In the delete() function:

  * Check if the queue is empty. If yes, display a message and return.
  
  * Traverse the list to find the index of the element with the highest priority (i.e., the lowest priority number).
  
  * Remove that element from the list using pop().
  
  * Display and return the deleted element.

## Program:

```python

class PriorityQueue:
    def __init__(self):
        self.queue = []

    def insert(self, item, priority):
        self.queue.append((item, priority))

    def delete(self):
        if not self.queue:
            print("Queue is empty.")
            return None
        
        # Find the element with the highest priority (lowest number)
        min_priority_index = 0
        for i in range(1, len(self.queue)):
            if self.queue[i][1] < self.queue[min_priority_index][1]:
                min_priority_index = i
        
        item = self.queue.pop(min_priority_index)
        print(f"Deleted item: {item[0]} with priority {item[1]}")
        return item[0]
```
## Output:
![image](https://github.com/user-attachments/assets/6ad489c7-6a72-40a3-a535-a1364264be3e)

## Result:
The delete() function removes the element with the highest priority from the priority queue and displays it.

