# print-alternate-nodes
class Node: #node creation
    def __init__(self,data):
        self.data=data
        self.next=None
class Llist: #main logic for list
    def __init__(self):
        self.head=None
    def build(self,data):
        new_node=Node(data) #calling Node class for creation of new_node
        if self.head is None:
            self.head=new_node
        else:
            temp=self.head
            while temp.next is not None:
                temp=temp.next
            temp.next=new_node
    def print_alternate_nodes(self):
        temp = self.head
        index = 0
        while temp is not None:
            if index % 2 != 0:
                print(temp.data, end="->")
            temp = temp.next
            index += 1
        print("None")
    
    def display(self):
        temp=self.head
        while temp is not None:
            print(temp.data,end="->")
            temp=temp.next
        print("None")
l1=Llist()
l1.build(1)
l1.build(2)
l1.build(3)
l1.build(8)
l1.display()
print("alternate nodes")
l1.print_alternate_nodes()

