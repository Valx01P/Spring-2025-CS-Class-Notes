\(- Dynamic \rightarrow O(1)\)
\(- Insert \rightarrow O(1)\)
\(- Reverse \rightarrow O(1)\)

\(\implies Linked List\)

---

- Singly Linked List
- Doubly Linked List
- Circular Linked List

#### LinkedList.java
```java
import java.util.NoSuchElementException;

public class LinkedList <T>{
	private class Node<T> {
		private T data;
		private Node<T> next;
		private Node() {
			data = null;
			next = null;
		}
	}
	private int size;
	private Node<T> head;
	
	
	public LinkedList() {
		size = 0;
		head = null;
		
	}
	
	public void addFirst(T data) {
		add(0, data);
//		Node<T> newNode = new Node<T>();
//		newNode.data = data;
//		newNode.next = head;
//		head = newNode;
//		size++;
	}
	
	public void addLast(T data) {
		add(size, data);
//		Node<T> newNode = new Node<>();
//		newNode.data = data;
//		newNode.next = null;
//		Node<T> temp = head;
//		for(int i = 0; i < size-1; i++)
//			temp = temp.next;
//		temp.next = newNode;
//		size++;
	}
	
	public void add(T data) {
		addLast(data);
	}
	
	public void add(int index, T data) {
		if(index < 0 || index > size)
			throw new IndexOutOfBoundsException();
		Node<T> newNode = new Node<>();
		newNode.data = data;
		if(index == 0) {
			newNode.next = head;
			head = newNode;
			size++;
			return;
		}
		Node<T> temp = head;
		for(int i = 0; i < index-1; i++)
			temp = temp.next;
		newNode.next = temp.next;
		temp.next = newNode;
		size++;
	}
	
	public int size() {
		return size;
	}
	
	public T get(int index) {
		if(index < 0 || index >= size)
			throw new NoSuchElementException();
		if(index == 0) {
			return head.data;
		}
		Node<T> temp = head;
		for(int i = 0; i < index; i++)
			temp = temp.next;
		return temp.data;
	}
	
	public T getFirst() {
		return get(0);
	}
	
	public T getLast() {
		return get(size-1);
	}
	
	public void set(int index, T data) {
		if(index < 0 || index >= size)
			throw new IndexOutOfBoundsException();
		Node<T> temp = head;
		for(int i = 0; i < index; i++)
			temp = temp.next;
		temp.data = data;
	}
	
	public void removeFirst() {
		remove(0);
	}
	
	public void removeLast() {
		remove(size-1);
	}
	
	public void remove() {
		removeLast();
	}
	
	public void remove(int index) {
		if(index < 0 || index > size)
			throw new IndexOutOfBoundsException();
		if(index == 0) {
			head = head.next;
			size--;
		}
		Node<T> temp = head;
		for(int i = 0; i < index-1; i++)
			temp = temp.next;
		Node<T> temp2 = temp.next;
		temp.next = temp2;
		size--;
	}
	
	public boolean contains(T data) {
		Node<T> temp = head;
		for(int i = 0; i < size; i++) {
			if(temp.data.equals(data))
				return true;
			temp = temp.next;
		}
		return false;
	}
	
	public String toString() {
		Node<T> temp = head;
		if (size == 0)
			return "[]";
		String str = "[";
		while(temp.next != null) {
			str = str + temp.data + ", ";
			temp = temp.next;
		}
		str = str + temp.data + "]";
		return str;
	}
	
	public void clear() {
		head = null; // makes head value and next to null
		size = 0;
		return;
	}
	
}
```

#### main.java
```java

public class main {

	public static void main(String[] args) {
		LinkedList list = new LinkedList();
		list.addFirst(5);
		list.addFirst(7);
		list.addLast(4);
		list.add(25);
		list.add(0,30);
		// if there is a toString, it automatically uses it
		System.out.println(list);
		list.add(2,17);
//		System.out.println(list.getFirst());
//		System.out.println(list.getLast());
//		System.out.println(list.get(3));
		list.set(1, 100);
		System.out.println(list);
		list.clear();
		System.out.println(list);

	}

}

```


(3+h)(3+h)(3+h)
(9 + 3h + 3h + h^2)(3+h)
27 + 9h + 6h + 3h^2 + 6h + 3h^2 + 3h^2 + h^3

h^3 + 9h^2 + 21h + 27


'hey can i talk with you'