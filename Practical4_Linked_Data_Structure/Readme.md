class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

class LinkedList:
    # ... (previous code)

    def append(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        current = self.head
        while current.next:
            current = current.next
        current.next = new_node

# Test the append method
ll = LinkedList()
ll.append(1)
ll.append(2)
ll.append(3)

class LinkedList:
    # ... (previous code)

    def display(self):
        elements = []
        current = self.head
        while current:
            elements.append(current.data)
            current = current.next
        print(" -> ".join(map(str, elements)))

# Test the display method
ll.display()

class LinkedList:
    # ... (previous code)

    def insert(self, data, position):
        new_node = Node(data)
        if position == 0:
            new_node.next = self.head
            self.head = new_node
            return
        current = self.head
        for _ in range(position - 1):
            if current is None:
                raise IndexError("Position out of range")
            current = current.next
        new_node.next = current.next
        current.next = new_node

# Test the insert method
ll.insert(4, 1)
ll.display()

class LinkedList:
    # ... (previous code)

    def delete(self, data):
        if not self.head:
            return
        if self.head.data == data:
            self.head = self.head.next
            return
        current = self.head
        while current.next:
            if current.next.data == data:
                current.next = current.next.next
                return
            current = current.next

# Test the delete method
ll.delete(2)
ll.display()

class LinkedList:
    # ... (previous code)

    def search(self, data):
        current = self.head
        position = 0
        while current:
            if current.data == data:
                return position
            current = current.next
            position += 1
        return -1

# Test the search method
print(ll.search(4))  # Output: 1
print(ll.search(5))

class LinkedList:
    # ... (previous code)

    def reverse(self):
        prev = None
        current = self.head
        while current:
            next_node = current.next
            current.next = prev
            prev = current
            current = next_node
        self.head = prev

# Test the reverse method
ll.reverse()
ll.display() 

class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

def mergeTwoLists(list1: ListNode, list2: ListNode) -> ListNode:
    dummy = ListNode(0)
    current = dummy
    
    while list1 and list2:
        if list1.val <= list2.val:
            current.next = list1
            list1 = list1.next
        else:
            current.next = list2
            list2 = list2.next
        current = current.next
    
    if list1:
        current.next = list1
    if list2:
        current.next = list2
    
    return dummy.next

    class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

def removeNthFromEnd(head: ListNode, n: int) -> ListNode:
    dummy = ListNode(0)
    dummy.next = head
    fast = slow = dummy
    
    # Move fast pointer n nodes ahead
    for _ in range(n):
        fast = fast.next
    
    # Move both pointers until fast reaches the end
    while fast.next:
        fast = fast.next
        slow = slow.next
    
    # Remove the nth node
    slow.next = slow.next.next
    
    return dummy.next