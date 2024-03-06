#include<stdio.h>

typedef struct node
{
	int data;
	struct node* next;
}Node;

int main()
{
	Node* root = NULL, *iterator = NULL, *temp = NULL;
	int num;

	root = (Node *)malloc(sizeof(Node));
	root->data =0;
	root->next = NULL;
	iterator = root;

	printf("Enter int for 5 linked-list\n");

	for (int i = 0; i < 4; i++) {
		scanf("%d", &num);
		temp = (Node*)malloc(sizeof(Node));
		temp->data = num;
		temp->next = NULL;
		iterator->next = temp;
		iterator = iterator->next;
	}

	PrintLinkedList(root);

	return 0;
}