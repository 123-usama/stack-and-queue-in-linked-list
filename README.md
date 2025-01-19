# stack-and-queue-in-linked-list
My first github repository
<br>
Aurthor- Muhammad usama
<br>
SECTION: 3 EVENING A
<br>
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
class Stack:
    def __init__(self):
        self.top = None
    def push(self, data):
        node = Node(data)
        node.next = self.top
        self.top = node
    def pop(self):
        if self.top is None:
            return None
        data = self.top.data
        self.top = self.top.next
        return data
class Queue:
    def __init__(self):
        self.front = None
        self.rear = None
    def enqueue(self, data):
        node = Node(data)
        if self.rear is None:
            self.front = self.rear = node
        else:
            self.rear.next = node
            self.rear = node
    def dequeue(self):
        if self.front is None:
            return None
        data = self.front.data
        self.front = self.front.next
        if self.front is None:
            self.rear = None
        return data
