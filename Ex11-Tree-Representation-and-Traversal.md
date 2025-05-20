# Ex11 Tree Representation and Traversal
## DATE:
## AIM:
To write a C function to perform post order traversal of a binary tree.

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```
/*
Program to perform post order traversal of a binary tree.
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/

#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

struct node {
    
    int data;
    struct node *left;
    struct node *right;
  
};

struct node* insert( struct node* root, int data ) {
		
	if(root == NULL) {
	
        struct node* node = (struct node*)malloc(sizeof(struct node));

        node->data = data;

        node->left = NULL;
        node->right = NULL;
        return node;
	  
	} else {
      
		struct node* cur;
		
		if(data <= root->data) {
            cur = insert(root->left, data);
            root->left = cur;
		} else {
            cur = insert(root->right, data);
            root->right = cur;
		}
	
		return root;
	}
}

/* 
node is defined as  

struct node {
    
    int data;
    struct node *left;
    struct node *right;
  
};

*/
void postOrder( struct node *root) {


if(root==NULL)
return;
postOrder(root->left);
postOrder(root->right);
printf("%d ",root->data);
}


int main() {
  
    struct node* root = NULL;
    
    int t;
    int data;

    scanf("%d", &t);

    while(t-- > 0) {
        scanf("%d", &data);
        root = insert(root, data);
    }
  
	postOrder(root);
    return 0;
}

```

## Output:

![Screenshot 2025-05-20 213854](https://github.com/user-attachments/assets/2aa49af3-4025-496f-b190-74085bfebb97)


## Result:
Thus, the function to perform post order traversal of a binary tree is implemented successfully
