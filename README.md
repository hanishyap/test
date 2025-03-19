


#include<stdio.h>
#include<conio.h>
#define MAX 4

int stack[MAX], item;
int top = -1;

void push()
{
	if (top == (MAX-1))
			printf("\n\nStack is Overflow");
	else
	{
		printf("\nEnter a element to be pushed: ");
		scanf("%d", &item);		
		stack[++top] = item;
	}
}

void pop()
{
	int ret;
	if(top == -1)
		printf("\n\nStack is Underflow");
	else
	{
		ret = stack[top--];
		printf("\nPopped element is %d", ret);
	}
}

void display()
{
	int i;
	printf("\nThe stack contents are:");
	if(top == -1)
		printf("\nStack is Empty");
	else
	{
		for(i=top; i>=0; i--)
		{
				printf("\n ------\n| %d |", stack[i]);
				printf("\n");
		}
	}
}

void main()
{
	int ch;
	clrscr();
	while(1)
	{
		printf("\n\n----MAIN MENU----\n");
		printf("\n1. PUSH (Insert) in the Stack");
		printf("\n2. POP (Delete) from the Stack");
		printf("\n3. Display elements from the Stack");
		printf("\n4. Exit (End the Execution)");
		printf("\nEnter Your Choice: ");
		scanf("%d", &ch);
		switch(ch)
		{
			case 1:push();
					 break;
			case 2:pop();
    				 break;
    		case 3:display();
					 break;
			case 4:exit(0); 
    		default: printf("\nEnter a Valid Choice");
   	}
	}	
	getch();
}	


