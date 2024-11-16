# stack using array
#include<iostream>
using namespace std;
int top=-1;
int size,stack[100];
bool isEmpty(){
    if(top==-1)
    {   //cout<<"\nstack is underflow\n ";
        return true;
    }
    else{
        return false;
    }
}
bool isFull(){
    if(top==size-1)
    {   //cout<<"\nstack is overflow \n";
        return true;
    }
    else{
        return false;
    }
}
int peek(){
    if(isEmpty()){
        cout<<"stack is empty\n";
    }
    else{
        return stack[top];    
    }
}
int push(int a){
    if(isFull()){
        cout<<"stack is overflow\n";
    }
    else{
        top++;
        stack[top] = a;
        return top;
    }
}
int pop(){
    if(isEmpty()){
        cout<<"stack is underflow\n";
    }
    else{
        int x;
        x=stack[top];
        top--;
        return x;
    }
}
int main(){
    cout<<"enter the size of stack : ";
    cin>>size;
for(int i=0;i<size;i++){
    int a;
    cout<<"enter the element you want insert : ";
    cin>>a;
    // push operation
    push(a);
}
int i = top;
    cout<<"after applying the push operation stack is : \n";
    while(i>=0){
        cout<<stack[i]<<" \n";
        i--;
    }
    // isfull operation
    isFull();
    //peek operation
    cout<<"peek element in stack is : "<<peek()<<endl;
    // pop operation
    pop();
    i = top;
    cout<<"after applying pop operation stack is : \n";
    while(i>=0){
        cout<<stack[i]<<" \n";
        i--;
    }
    // isempty operation
   isEmpty();
    return 0;
}
