# DS-1
DS code
#include<stdio.h>
#define max 20
int stk[max];
int top=-1,i,ch;
int push()
{
     if(top==max-1)
        {
            printf("\nstack is full!!\n");
        }
     else
        {
            printf("\nenter element to be inserted: \n");
            scanf("%d",&stk[top+1]);
            top++;
        }
        return 0;
}
int pop()
{
     if(top==-1)
     {
        printf("\nstack is empty\n");
     }
     else
     {
        printf("\n%d is deleted\n", stk[top]);
        top--;
     }
     return 0;
}
int display()
{
    printf("\nelements of stack\n");
    for(i=0;i<=top;i++)
        {
            printf("\n%d\n",stk[i]);
        }
        return 0;
}
int main()
{
    do
    {
        printf("\n--------------STACK-------------\n");
        printf("\nEnter choice\n1.push\n2.pop\n3.display\n4.quit:\n");
        printf("\n---------------------------\n");
        scanf("%d",&ch);
        switch(ch)
        {
        case 1:
            {
               push();
               break;
            }
        case 2:
            {
                pop();
                break;
            }
        case 3:
            {
                display();
                break;
            }
        }
    }
    while(ch!=4);
    printf("\nExiting!!!");
    return 0;
}
