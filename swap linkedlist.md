```java
// Java program to swap two given nodes of a linked list
public class Solution {

	// Represent a node of the singly linked list
	class Node {
		int data;
		Node next;

		public Node(int data)
		{
			this.data = data;
			this.next = null;
		}
	}

	// Represent the head and tail of the singly linked list
	public Node head = null;
	public Node tail = null;

	// addNode() will add a new node to the list
	public void addNode(int data)
	{
		// Create a new node
		Node newNode = new Node(data);

		// Checks if the list is empty
		if (head == null) {
			// If list is empty, both head and
			// tail will point to new node
			head = newNode;
			tail = newNode;
		}
		else {
			// newNode will be added after tail such that
			// tail's next will point to newNode
			tail.next = newNode;
			// newNode will become new tail of the list
			tail = newNode;
		}
	}

	// swap() will swap the given two nodes
	public void swap(int n1, int n2)
	{
		Node prevNode1 = null, prevNode2 = null,
			node1 = head, node2 = head;

		// Checks if list is empty
		if (head == null) {
			return;
		}

		// If n1 and n2 are equal, then
		// list will remain the same
		if (n1 == n2)
			return;

		// Search for node1
		while (node1 != null && node1.data != n1) {
			prevNode1 = node1;
			node1 = node1.next;
		}

		// Search for node2
		while (node2 != null && node2.data != n2) {
			prevNode2 = node2;
			node2 = node2.next;
		}

		if (node1 != null && node2 != null) {

			// If previous node to node1 is not null then,
			// it will point to node2
			if (prevNode1 != null)
				prevNode1.next = node2;
			else
				head = node2;

			// If previous node to node2 is not null then,
			// it will point to node1
			if (prevNode2 != null)
				prevNode2.next = node1;
			else
				head = node1;

			// Swaps the next nodes of node1 and node2
			Node temp = node1.next;
			node1.next = node2.next;
			node2.next = temp;
		}
		else {
			System.out.println("Swapping is not possible");
		}
	}

	// display() will display all the
	// nodes present in the list
	public void display()
	{
		// Node current will point to head
		Node current = head;

		if (head == null) {
			System.out.println("List is empty");
			return;
		}
		while (current != null) {
			// Prints each node by incrementing pointer
			System.out.print(current.data + " ");
			current = current.next;
		}
		System.out.println();
	}

	public static void main(String[] args)
	{

		Solution sList = new Solution();

		// Add nodes to the list
		sList.addNode(1);
		sList.addNode(2);
		sList.addNode(3);
		sList.addNode(4);
		sList.addNode(5);
		sList.addNode(6);
		sList.addNode(7);

		System.out.println("Original list: ");
		sList.display();

		// Swaps the node 2 with node 5
		sList.swap(6, 1);

		System.out.println("List after swapping nodes: ");
		sList.display();
	}
}
```
