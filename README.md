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
