# Insert-at-end-LL
Insert a node at the end of a singly linked list
//Insert at end of singly linked list
#include<iostream>
using namespace std;

struct Node{
	int data;
	Node* next;
	Node(int x){
		data=x;
		next=NULL;
	}
};

Node* insertAtEnd(Node* head,int y){
	Node* temp = new Node(y);
	if(head=NULL){
		return temp;
	}
	Node* curr=head;
	while(curr->next!=NULL){
		curr=curr->next;
	}
	curr->next=temp;
	return head;
}

Node* getLength(Node* head){
	int count=0;
	Node* curr=head;
	while(curr!=NULL){
		count++;
		curr=curr->next;
	}
	cout<<count;
}

Node* printList(Node* head){
	Node* curr=head;
	while(curr!=NULL){
		cout<<curr->data;
		curr=curr->next;
	}
}

int main(){
	Node* head = NULL;
	head=insertAtEnd(head,1);
	head=insertAtEnd(head,2);
	head=insertAtEnd(head,3);
	head=insertAtEnd(head,4);
	head=insertAtEnd(head,5);
	printList(head);
	cout<<"Length of Linked list: "<<getLength(head);
	return 0;
}
