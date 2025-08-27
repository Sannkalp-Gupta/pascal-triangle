# pascal-triangle
# made it using loops and some understanding of rows and column
#include<stdio.h>
#include<stdlib.h>
int main()
{
	while(1)
	{
		int s,n,a,b,q;
		char o;
		system("clear");
		printf("Calculator\n\n");
		printf("Press + for addition\n");
		printf("Press - for substarction\n");
		printf("Press * for multiplication\n");
		printf("Press / for division\n");
		printf("Enter q to quit:\n\n");
		printf("Enter the operation which you want to perform:");
		fflush(stdin);
		scanf("%c",&o);
		system("clear");
		switch(o)
		{
			case '+':
				printf("Addition:\n");
				printf("If you want to discontinue at any point enter 0\n\n");
				s=0;
				a=1;
				while(1)
				{
					printf("Enter the %d number=",a);
					scanf("%d",&n);
					if(n==0)
					break;
					s=s+n;
					a++;
				}
				printf("\nSum=%d",s);
				break;
			case '-':
				printf("Substraction:\n\n");
				printf("Enter the first number=");
				scanf("%d",&s);
				printf("Enter the second number=");
				scanf("%d",&n);
				a=s-n;
				printf("\nDifference=%d",a);
				break;
			case '*':
				printf("Multiplication:\n");
				printf("If you want to discontinue at any point enter 1\n\n");
				s=1;
				a=1;
				while(1)
				{
					printf("Enter the %d number=",a);
					scanf("%d",&n);
					if(n==1)
					break;
					s=s*n;
					a++;
				}
				printf("\nProduct=%d",s);
				break;
			case '/':
				printf("Division:\n\n");
				printf("Enter the dividend=");
				scanf("%d",&s);
				printf("Enter the divisor=");
				scanf("%d",&n);
				a=s/n;
				b=s%n;
				printf("\nQuotient=%d\n",a);
				printf("\nRemainder=%d",b);
				break;
			case 'q':
				exit(0);
		}
		printf("\n\nIf you want to quit calculator,Enter 0 or otherwise enter any integer:");
		scanf("%d",&q);
		if(q==0)
		{
			break;
		}
	}
	return 0;
}
