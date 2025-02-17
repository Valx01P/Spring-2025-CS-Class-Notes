
main.java
```java
// Assignment 4: BST
// By Pablo Valdes

public class main {
    public static void main(String[] args) {
        BST tree = new BST();

        tree.BSTInsert(7);
        tree.BSTInsert(2);
        tree.BSTInsert(5);
        tree.BSTInsert(6);
        tree.BSTInsert(12);
        tree.BSTInsert(420);

        System.out.println(tree.TreeMinimum()); // 2
        System.out.println(tree.TreeMaximum()); // 420

        System.out.println(tree.TreeSearch(69)); // false
        System.out.println(tree.TreeSearch(420)); // true
    }
}
```

BST.java
```java
public class BST {
    private class Node {
        private int key;
        private Node left, right;

        private Node(int key) {
            this.key = key;
            this.left = null;
            this.right = null;
        }
    }

    private Node root;

    public BST() {
        root = null;
    }

    public void BSTInsert(int key) {
        Node newNode = new Node(key);
        Node y = null;
        Node x = root;

        while (x != null) {
            y = x;
            if (newNode.key < x.key) {
                x = x.left;
            } else {
                x = x.right;
            }
        }

        if (y == null) {
            root = newNode; // The tree was empty
        } else if (newNode.key < y.key) {
            y.left = newNode;
        } else {
            y.right = newNode;
        }
    }

    public int TreeMinimum() {
        if (root == null) {
            System.out.println("Tree is empty");
            return -1;
        }
        Node minNode = root;
        while (minNode.left != null) {
            minNode = minNode.left;
        }
        return minNode.key;
    }

    public int TreeMaximum() {
        if (root == null) {
            System.out.println("Tree is empty");
            return -1;
        }
        Node maxNode = root;
        while (maxNode.right != null) {
            maxNode = maxNode.right;
        }
        return maxNode.key;
    }

    public boolean TreeSearch(int key) {
        Node x = root;
        while (x != null) {
            if (key == x.key) {
                return true;
            } else if (key < x.key) {
                x = x.left;
            } else {
                x = x.right;
            }
        }
        return false;
    }
}
```