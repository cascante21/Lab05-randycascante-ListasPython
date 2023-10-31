class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class LinkedList:
    def __init__(self):
        self.head = None

    def add_node(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
        else:
            current = self.head
            while current.next:
                current = current.next
            current.next = new_node

    def delete_node(self, value):
        if not self.head:
            print("La lista está vacía.")
            return

        if self.head.data == value:
            self.head = self.head.next
            return

        current = self.head
        while current.next:
            if current.next.data == value:
                current.next = current.next.next
                return
            current = current.next

    def add_node_at_beginning(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node

    def add_node_at_end(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
        else:
            current = self.head
            while current.next:
                current = current.next
            current.next = new_node

    def search_node(self, value):
        current = self.head
        while current:
            if current.data == value:
                print(f"El nodo con valor {value} existe en la lista.")
                return
            current = current.next
        print(f"El nodo con valor {value} no existe en la lista.")

    def print_list(self):
        current = self.head
        while current:
            print(current.data, end=" -> ")
            current = current.next
        print("None")

    def get_nth_element(self, index):
        current = self.head
        count = 0
        while current:
            if count == index:
                print(f"Elemento en la posición {index}: {current.data}")
                return
            count += 1
            current = current.next
        print(f"No existe un elemento en la posición {index}.")

if __name__ == "__main__":
    linked_list = LinkedList()

    linked_list.add_node(1)
    linked_list.add_node(2)
    linked_list.add_node(3)
    linked_list.add_node(4)
    linked_list.add_node(5)

    linked_list.print_list()

    linked_list.delete_node(3)
    linked_list.print_list()

    linked_list.add_node_at_beginning(0)
    linked_list.print_list()

    linked_list.add_node_at_end(6)
    linked_list.print_list()

    linked_list.search_node(4)
    linked_list.search_node(7)

    linked_list.get_nth_element(2)
    linked_list.get_nth_element(6)
