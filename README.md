# TREES
In this we will document the tree data structure/

************  INTRODUCTION TO TREES AND TYPES OF TREES ***************

- Binay Trees: These trees have at most two nodes(As the word Suggest).
- Sub Trees: Subtrees of any node either left or right.
- Root: The top most node of the tree is known as Root od tree.
- Children: node below any node is called child node.
- lead Node: Node who has no childern is called leaf node.
- Ancestors: Node above any node are called Ancestors

*********************** TYPES OF BINARY TREES ************************
- Full Binary Tree: every nodes have either two childern or Zero Childern.
- Complete Binary Tree: All the levels must be filled except the last Level. The last level all the nodes in left as possible.
- Perfect Binary Tree: All the leaf node must be in the same level.
- Balanced Binary Tree: The heihgt of the tree must be Log(N). Where N is the no. of Nodes.
- Degenerate Binary Tree: The stright tree like linked list.

********* REPRESENTATION OF BINARY TREE IN JAVA ************

- left Reference | Data | Right Reference : this is how the node in Binary Tree will be represent
  class Node{
    int data;
    Node left;
    NOde right;
  public class Node(Key){
   data = Key;
    }
  }

  - In the main function:
     main(){
      Node root = new Node(1);  //calling the constructor using new Node to assign the value 1 to the root Node.
      root.left = new Node(2);  //assigning values to left of root
      root.right = new Node(3); // assgning values to right of root
      root.right.left = new Node(5); 
    }

******************** TRAVERSAL IN TREE *************************

- Inorder Traversal : Left | Root | Right
- Pre Order: Root | Left | Right
- Post order: Left | Right | Root

********** PRE ORDER TRAVERSAL *************
import java.util.ArrayList;
import java.util.List;

// Node class for
// the binary tree
class Node {
    int data;
    Node left;
    Node right;
   Node(int val) {
        data = val;
        left = null;  
        right = null;
    }
}

public class BinaryTreeTraversal {
    // Function to perform preorder traversal
    // of the tree and store values in 'arr'
    static void preorder(Node root, List<Integer> arr) {
        // If the current node is NULL
        // (base case for recursion), return
        if (root == null) {
            return;
        }
        // Push the current node's
        // value into the list
        arr.add(root.data);
        // Recursively traverse
        // the left subtree
        preorder(root.left, arr);
        // Recursively traverse
        // the right subtree
        preorder(root.right, arr);
    }
    static List<Integer> preOrder(Node root) {
        // Create an empty list to
        // store preorder traversal values
        List<Integer> arr = new ArrayList<>();
        // Call the preorder traversal function
        preorder(root, arr);
        // Return the resulting list
        // containing preorder traversal values
        return arr;
    }

  public static void main(String[] args) {
        Node root = new Node(1);
        root.left = new Node(2);
        root.right = new Node(3);
        root.left.left = new Node(4);
        root.left.right = new Node(5); // Getting preorder traversal
        List<Integer> result = preOrder(root);
       // Displaying the preorder traversal result
        System.out.print("Preorder Traversal: ");
        // Output each value in the
        // preorder traversal result
        for (int val : result) {
            System.out.print(val + " ");
        }
        System.out.println();
    }
}

Time Complexity: O(n) "n is the number of node"
Space complexity: O(n)

************* INORDER TRAVERSAL *******************

class Node{
  int val;
  Node right;
  Node left;

public Node(data){
  Node.val = data;
  Node.right = null;
  Node.left = null;
 }
}
public class BinaryTreeTraversal{
  static void Inorder(Node root, List<Integer> arr){
    if(root == null){
     return;
     }
    Inorder(root.left, arr);
    arr.add(root.data);
    Inorder(root.right, arr);
}
public static List<Integer> Inorder(Node root)
 {
  List<Integer> arr = new ArrayList<>();
  Inorder(root, arr)
  return arr;
 }
  public static void main(String[] args) {
        Node root = new Node(1);
        root.left = new Node(2);
        root.right = new Node(3);
        root.left.left = new Node(4);
        root.left.right = new Node(5);
   List<Integer> result = inOrder(root);
 System.out.print("Inorder Traversal: ");
        for (int val : result) {
            System.out.print(val + " ");
        }
        System.out.println();
    }
