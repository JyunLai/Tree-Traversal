#include <iostream>
using namespace std;

struct node{
    struct node *left=NULL;
    struct node *right=NULL;
    int data=0;
};
void insert(node *root,int i){
    if(i==root->data){
        return;
    }
    else if(i>(root->data)){
        node *root1=(node *)malloc(sizeof(node));
        if(root->right==NULL){
            root1->data=i;
            root->right=root1;
            return;
        }
        else{
            insert(root->right,i);
        }
    }
    else if(i<(root->data)){
        node *root1=(node *)malloc(sizeof(node));
        if(root->left==NULL){
            root1->data=i;
            root->left=root1;
            return;
        }
        else{
            insert(root->left,i);
        }
    }
}
void Inorder(node *root){
    if(root->left!=NULL){
        Inorder(root->left);
        cout<<" ";
    }
    cout<<root->data;
    if(root->right!=NULL){
        cout<<" ";
        Inorder(root->right);
    }
}
void Preorder(node *root){
    cout<<root->data;
    if(root->left!=NULL){
        cout<<" ";
        Preorder(root->left);
    }
    if(root->right!=NULL){
        cout<<" ";
        Preorder(root->right);
    }
}
void Postorder(node *root){
    if(root->left!=NULL){
        Postorder(root->left);
        cout<<" ";
    }
    if(root->right!=NULL){
        Postorder(root->right);
        cout<<" ";
    }
    cout<<root->data;
}
int main(int argc, const char * argv[]) {
    int i;
    node root;
    cin>>i;
    root.data=i;
    while(cin>>i){
        insert(&root,i);
    }
    Inorder(&root);
    cout<<endl;
    Preorder(&root);
    cout<<endl;
    Postorder(&root);
    cout<<endl;
    return 0;
}
