Reversed Linked List method
```java
    public void reverse() {
        Node<T> prev = null;
        Node<T> current = head;
        Node<T> next = null;

        while (current != null) {
            next = current.next; 
            current.next = prev;
            prev = current;
            current = next;
        }

        head = prev;
    }
```