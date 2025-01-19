# stack-and-queue-in-linked-list
My first github repository
<br>
Aurthor- Muhammad usama
<br>
SECTION: 3 EVENING A
<br>
class Node:<br>
    def __init__(self, data):<br>
        self.data = data<br>
        self.next = None<br>
class Stack:<br>
    def __init__(self):<br>
        self.top = None<br>
    def push(self, data):<br>
        node = Node(data)<br>
        node.next = self.top<br>
        self.top = node<br>
    def pop(self):<br>
        if self.top is None:<br>
            return None<br>
        data = self.top.data<br>
        self.top = self.top.next<br>
        return data<br>
class Queue:<br>
    def __init__(self):<BR>
        self.front = None<Br>
        self.rear = None<br>
    def enqueue(self, data):<br>
        node = Node(data)<br>
        if self.rear is None:<br>
            self.front = self.rear = node<br>
        else:<br>
            self.rear.next = node<Br>
            self.rear = node<BR>
    def dequeue(self):<br>
        if self.front is None:<br>
            return None<br>
        data = self.front.data<br>
        self.front = self.front.next<br>
        if self.front is None:<br>
            self.rear = None>br>
        return data<br>
