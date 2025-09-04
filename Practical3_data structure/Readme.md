class stack:
    def __init__(self):
        self.items = []

    def is_empty(self):
        return len(self.items) == 0
    
    def push(self, item):
        self.items.append(item)

    def pop(self):
        if not self.is_empty():
            return self.items.pop()
        else:
            raise IndexError("stack is empty")
        
    def peek(self):
        if not self.is_empty():
            return self.items[-1]
        else:
            raise IndexError("stack is empty")
        
    def size(self):
        return len(self.items)

Stack = stack()
Stack.push(1)
Stack.push(2)
Stack.push(3)
print(Stack.pop())
print(Stack.peek())
print(Stack.size())

class Queue:
    def __init__(self):
        self.items = []

    def is_empty(self):
        return len(self.items) == 0
    
    def enqueue(self, item):
        self.items.append(item)

    def dequeue(self):
        if not self.is_empty():
            return self.items.pop(0)
        else:
            raise IndexError("Queue is empty")
        
    def front(self):
        if not self.is_empty():
            return self.items[0]
        else:
            raise IndexError("Queue is empty")
        
    def size(self):
        return len(self.items)
    
queue = Queue()
queue.enqueue(1)
queue.enqueue(2)
queue.enqueue(3)
print(queue.dequeue())
print(queue.front())
print(queue.size())