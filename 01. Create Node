#include<stdio.h>
#include<stdlib.h>
#include<conio.h>
//Structure of a Node
struct Node
{
	int data;
	struct Node *next;
};
struct Node *first = NULL;	//Points towards first Node
struct Node *last = NULL;	//Points towards the last node

//Note: The addition of new node will be at the end of the Linked List in this program
void addNode(int data)
{
	//Step1 Create a new node and assign its address to a temporary pointer variable
	struct Node *temp = (struct Node *) malloc(sizeof(struct Node));
	temp->data = data;
	temp->next = NULL;
	
	//Step2 Check whteher its first node
	if(first == NULL)		//if first is equal to NULL then its first node of linked list
	{
		first = temp;
		last = first;		//As its first node then first and last are same
	}
	else	//If its not the first node
	{
		//Step3 Traverse through all the Linked List and find the last link
		struct Node *p = first;
		while(p->next!=NULL)
		{
			p = p->next;
		}
		p->next = temp;		//Last Node whose link is NULL assign the adrress of the new node
		last = temp;
	}
}

void displayNodes()
{
	struct Node *p = first;
	while(p!=NULL)
	{
		printf("%d ",p->data);
		p = p->next;
	}
	printf("\n");
}
void lastNode()
{
	printf("%d ",last->data);
	printf("\n");
}
void main()
{
	addNode(12);		
	addNode(1242);		
	addNode(42);		
	addNode(42);		
	addNode(42);		
	addNode(1342);		
	addNode(1342);	
	addNode(1242);		
	addNode(2147483647);		
	
	lastNode();
	displayNodes();
	
	getch();
}
