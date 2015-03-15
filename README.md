//A Simple program to insert an element at the end of the Linked List in C++

#include<iostream.h>
#include<conio.h>
class LinkedList{

private:
struct node{
   int value;
   node *next;
}*head;

public:
LinkedList(){

     head = NULL;
}

void insert(int no){

	node *n = new node();
	n->value = no;
	n->next = NULL;

	if(head==NULL)
		head = n;

	else{
		node *n1 = head;
		while(n1->next!=NULL)
			n1=n1->next;
			n1->next=n;
	}

}

void show(){
	node *n = head;
	while(n->next!=NULL){
		cout<<n->value<<"\n";
		n = n->next;
	}
	cout<<n->value;

}
};

void main(){

clrscr();
LinkedList l;
l.insert(32);
l.insert(43);
l.insert(7);
l.insert(89);
l.insert(23);
l.insert(6);
l.show();
getch();
}
