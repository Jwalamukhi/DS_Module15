# Ex12 Binary Search Tree
## DATE:
## AIM:
To write a C function to insert the elements in the binary search tree

## Algorithm
1. 
2. 
3. 
4.  
5.   

## Program:
```
/*
Program to insert the elements in the binary search tree
Developed by: Jwalamukhi S
RegisterNumber:  212223040079
*/

struct node* insert(struct node* node, int key) {
   
    if(node==NULL)
    return newNode(key);
    if(key<node->key)
    node->left=insert(node->left,key);
    else if(key>node->key)
    node->right=insert(node->right,key);
    return node;
}
```

## Output:

![Screenshot 2025-05-20 214313](https://github.com/user-attachments/assets/43814f5b-b3ec-42ff-b66b-3eca271ede84)


## Result:
Thus, the C function to insert the elements in the binary search tree is implemented successfully.
