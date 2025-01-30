#### ArrayQueue.java
```java
import java.util.NoSuchElementException;

public class ArrayQueue <T>{
	private T[] q;
	private int front, rear, size, capacity;
	
	public ArrayQueue() {
		this(5);
	}
	
	public ArrayQueue(int capacity) {
		this.capacity = capacity;
		q = (T[]) new Object[capacity];
		size = front = rear = 0;
	}
	
	public int getSize() {
		return size;
	}
	
	public boolean isEmpty() {
		return getSize() == 0;
	}
	
	public boolean isFull() {
		return getSize() == this.capacity; // you don't need the this lmao
	}
	
	public void enQueue(T data) {
		if(isFull())
			throw new IndexOutOfBoundsException("Queue is full.");
		q[rear] = data;
		rear = (rear + 1) % capacity;
		size++;
	}
	
	public T deQueue() {
		if(isEmpty())
			throw new NoSuchElementException("Queue is Empty");
		T data = q[front];
		front = (front + 1) % capacity;
		size--;
		return data;
	}
	
	public T peek() {
		if(isEmpty())
			throw new NoSuchElementException("Queue is Empty");
		return q[front];
	}
	
	public String toString() {
		if(isEmpty())
			return "[]";
		String str = "[";
		int i = 0;
		for(i = 0; i < size-1; i++)
			str = str + q[(front + i) % capacity] + ", ";
		str = str + q[(front + 1) % capacity] + "]";
		return str;
	}
}

```


#### main.java
```java
public class main {

	public static void main(String[] args) {
		ArrayQueue q = new ArrayQueue();
		
		q.enQueue(5);
		
		
		System.out.println(q);
		System.out.println(q.isFull());

	}

}
```