#include <stdio.h>
#include <stdlib.h>

struct NODE
{
	int data;
	struct NODE *add;
} *start = NULL;

/* Create a NODE */
void create()
{
	struct NODE *p,*q;
	int n;
	printf("Enter a Number:-\n");
	scanf("%d",&n);
	p = (struct NODE*) malloc(sizeof(struct NODE));
	p->data = n;
	p->add = NULL;
	if(start == NULL)
	{
		start = p;
	}
	else
	{
		q = start;
		while(q->add != NULL)
		{
			q = q->add;
		}
		q->add = p;
	}
}

/* Insert a NODE at First Position */
void insert_at_first()
{
	struct NODE *p, *q;
	int n;
	printf("Enter a Number:-\n");
	scanf("%d",&n);
	q = start;
	p = (struct NODE*) malloc(sizeof(struct NODE));
	start = p;
	p->add = q;
	p->data = n;
}

/* Insert a NODE at Last Position */
void insert_at_last()
{
	struct NODE *p, *q;
	int n;
	printf("Enter a Number:- \n");
	scanf("%d",&n);
	p = (struct NODE*) malloc(sizeof(struct NODE));
	p->data = n;
	p->add = NULL;
	q = start;
	while(q->add != NULL)
	{
		q = q->add;
	}
	q->add = p;
}

/* Insert a NODE at a specific Position */
void insert_at_any_position()
{
	struct NODE *p, *q, *r;
	int n, pos, m=0;
	printf("Enter a Number:- ");
	scanf("%d",&n);
	printf("Enter the Position to insert a NODE:- ");
	scanf("%d",&pos);
	q = start;
	p = (struct NODE*) malloc(sizeof(struct NODE));
	while(q!= NULL)
	{
		m = m+1;
		if(pos == m)
		{
			r->add = p;
			p->add = q;
			break;
		}
		r = q;
		q = q->add;
	}
}

/* Delete a NODE From First Position */
void delete_at_first()
{
	struct NODE *p;
	p = start;
	start = p->add;
	free(p);
}

/* Delete a NODE From Last Position */
void delete_at_last()
{
	struct NODE *p, *q;
	p = start;
	while(p->add!= NULL)
	{
		q = p;
		p = p->add;
	}
	q ->add = NULL;
	free(p);
}

/* Delete a NODE From a specific Position */
void delete_at_any_position()
{
	struct NODE *p, *q;
	int pos, m=0;
	printf("Enter the Position:- ");
	scanf("%d",&pos);
	p = start;
	while(p->add!= NULL)
	{
		m=m+1;
		if(m == pos)
		{
			q->add = p->add;
			free(p);
			break;
		}
		q = p;
		p = p->add;
	}
}

/* Count the Number of NODEs. */
void count()
{
	struct NODE *p;
	int count = 0;
	p = start;
	while(p!=NULL)
	{
		count = count + 1;
		p = p->add;
	}
	printf("Numbers of NODEs in List: %d\n\n", count);
}

/* Sort the Linked List. */
void sort()
{
	struct NODE *p, *q;
	int r;
	p = start;
	while(p!=NULL)
	{
		q = p->add;
		while(q!=NULL)
		{
			if(p->data > q->data)
			{
				r = p->data;
				p->data = q->data;
				q->data = r;
			}
			q = q->add;
		}
		p = p->add;
	}
}

/* Search a Data in Linked List. */
void search()
{
	struct NODE *p;
	int search;
	int m = 0;
	printf("Enter searching element:- ");
	scanf("%d",&search);
	p = start;
	while(p!= NULL)
	{
		if(search == p->data)
		{
			m = m+1;
			break;
		}
		p = p->add;
	}
	if(m==1)
	{
		printf("FOUND\n");
	}
	else
	{
		printf("NOT FOUND\n");
	}
}

/* Reverse a Linked List */
void Reverse()
{
	struct NODE *p, *q, *current;
	q = NULL;
	current = start;
	while(current!= NULL)
	{
		p = current->add;
		current->add = q;
		q = current;
		current = p;
	}
	start = q;
}

/* Display the Linked List */
void display()
{
	struct NODE *p;
	p=start;
	while(p!=NULL)
	{
		printf("%d, ",p->data);
		p=p->add;
	}
	printf("\n\n");
}

/* Reverse and Display the Linked List */
void reverse_display()
{
	Reverse();
	printf("Reversed Linked List:- ");
	display();
	Reverse();
}

int main()
{
	int ch;
	while(1)
	{
		printf("Choice 1:  Create a NODE.\n");
		printf("Choice 2:  Insert a NODE at First Position.\n");
		printf("Choice 3:  Insert a NODE at Last Position.\n");
		printf("Choice 4:  Insert a NODE at a specific Position.\n");
		printf("Choice 5:  Delete a NODE From First Position.\n");
		printf("Choice 6:  Delete a NODE From Last Position.\n");
		printf("Choice 7:  Delete a NODE From a specific Position.\n");
		printf("Choice 8:  Count the Number of NODEs.\n");
		printf("Choice 9:  Sort the Linked List.\n");
		printf("Choice 10: Search a Data in Linked List.\n");
		printf("Choice 11: Reverse the Linked List.\n");
		printf("Choice 12: Display the Linked List.\n");
		printf("Choice 13: Reverse and Display the Linked List.\n");
		printf("Choice 14: End the Program.\n\n");
		printf("Enter Your Choice:- ");
		scanf("%d",&ch);
		printf("\n\n");

		switch(ch)
		{
			case 1:
			create();
			break;

			case 2:
			insert_at_first();
			break;

			case 3:
			insert_at_last();
			break;

			case 4:
			insert_at_any_position();
			break;

			case 5:
			delete_at_first();
			break;

			case 6:
			delete_at_last();
			break;

			case 7:
			delete_at_any_position();
			break;

			case 8:
			count();
			break;

			case 9:
			sort();
			break;

			case 10:
			search();
			break;

			case 11:
			Reverse();
			break;

			case 12:
			printf("Linked List:- ");
			display();
			break;

			case 13:
			reverse_display();
			break;

			case 14:
			printf("\a");
			exit(0);
		}
	}
	return 0;
}