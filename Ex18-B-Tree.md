# Ex4C B-Tree
## DATE: 25-05-2025
## AIM:
To write a C function to delete an element in a B Tree.
## Algorithm
1.	Start
2.	Try to delete the item from the node using delValFromNode. If not found, print "Not present" and return.
3.	If the node's count is 0 after deletion, set tmp to the current node and update myNode to its first linker child.
4.	Free the tmp node.
5.	Update the global root to the new myNode.# Ex4B AVL Tree – Rotation
## DATE: 24-05-2025
## AIM:
To write a C function to perform right rotation in an AVL Tree.

## Algorithm
1.	Start
2.	Set y to the left child of x.
3.	Set the left child of x to be the right child of y.
4.	Set the right child of y to be x.
5.	Update the height of x and y.
6.	Return y as the new root after rotation.
7.	End

## Program:
```
/*
Program to perform right rotation in AVL Tree
Developed by: MUKESH R
RegisterNumber: 212223240100

typedefstruct node
{
int data;
struct node*left,*right; int ht;
}node;
node *insert(node*,int);
//node*Delete(node*,int); void preorder(node*);
//void inorder(node*); int height( node *); node*rotateright(node*); node*rotateleft(node*); node *RR(node *); node *LL(node *); node *LR(node *);
node*RL(node*);
*/
node * rotateright(node *x)
{
node *y; y=x->left;
x->left=y->right; y->right=x;
 
x->ht=height(x); y->ht=height(y); return(y);
}

*/
```

## Output:

![image](https://github.com/user-attachments/assets/dbad47a2-5264-4dd7-b9cd-47960a07b692)



## Result:
Thus, the function to perform right rotation in an AVL Tree is implemented successfully.

6.	Return after deletion.
7.	End


## Program:
```
/*
Program to write a C function to delete an element in a B Tree
Developed by: Istin B
RegisterNumber: 212223040068

struct BTreeNode{
int item[MAX+1], count;
struct BTreeNode*linker[MAX+1];
};

struct BTreeNode*root;*/
voiddelete(int item, struct BTreeNode*myNode) { struct BTreeNode*tmp; if(!delValFromNode(item, myNode)){ printf("Not present\n");
return;
} else{
if(myNode->count ==0) { tmp = myNode;
myNode=myNode->linker[0]; free(tmp);
}
}
root=myNode; return;
}

*/
```

## Output:

![image](https://github.com/user-attachments/assets/d26dcca1-54b2-48b7-981d-abc925c7a3e8)



## Result:
Thus, the C function to delete an element in a B Tree is implemented successfully.
