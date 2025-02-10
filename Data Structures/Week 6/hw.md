#### main.java
```java
import java.util.Scanner;

public class main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter an infix expression:");
        String infix = scanner.nextLine(); // ex. input: (A+B)*C+D
        System.out.println("Postfix: " + InfixConverter.toPostfix(infix));
        scanner.close();
    }
}

```

#### InfixConverter.java
```java
public class InfixConverter {

    private static int getPriority(char op) {
        if (op == '+' || op == '-') return 1;
        if (op == '*' || op == '/') return 2;
        return 0;
    }

    public static String toPostfix(String infix) {
        ArrayStack<Character> stack = new ArrayStack<>(infix.length());
        StringBuilder output = new StringBuilder();

        System.out.println("Processing: " + infix);

        for (int i = 0; i < infix.length(); i++) {
            char c = infix.charAt(i);
            System.out.println("Index " + i + " = " + c);

            if (Character.isLetterOrDigit(c)) { 
                output.append(c);
                System.out.println("Added to output: " + output);
            } else if (c == '(') {
                stack.push(c);
                System.out.println("Pushed to stack: " + c);
            } else if (c == ')') {
                while (!stack.isEmpty() && stack.peek() != '(') {
                    output.append(stack.pop());
                }
                stack.pop(); 
            } else {
                while (!stack.isEmpty() && getPriority(stack.peek()) >= getPriority(c)) {
                    output.append(stack.pop());
                    System.out.println("Popped from stack to output: " + output);
                }
                stack.push(c);
                System.out.println("Pushed to stack: " + c);
            }
        }

        while (!stack.isEmpty()) {
            output.append(stack.pop());
            System.out.println("Final popping from stack to output: " + output);
        }

        return output.toString();
    }
}
```

#### ArrayStack.java
```java
public class ArrayStack<T> {
	
    private int top;
    private T[] stack;

    public ArrayStack(int size) {
        top = 0;
        stack = (T[]) new Object[size];
    }

    public boolean isEmpty() {
        return top == 0;
    }

    public void push(T data) {
        if (top == stack.length) {
            resize();
        }
        stack[top++] = data;
    }

    public T pop() {
        if (isEmpty()) {
            return null;
        }
        return stack[--top];
    }

    public T peek() {
        if (isEmpty()) {
            return null;
        }
        return stack[top - 1];
    }

    private void resize() {
        T[] newStack = (T[]) new Object[stack.length * 2];
        for (int i = 0; i < stack.length; i++) {
            newStack[i] = stack[i];
        }
        stack = newStack;
    }
}
```