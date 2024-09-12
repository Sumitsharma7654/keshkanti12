#include <stdio.h>

int main()
{
    int n,m,l,k,a[20];
    printf("enter no. of elements");
    scanf("%d",&n);
    printf("enter no. ");
    for(int i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    printf("enter your opertion\n1-: display\n2-: insertion\n3-:deletion\n");
    scanf("%d",&m);
    switch(m)
    {
        case 1:
        {
            printf("entered elements are ");
            for(int i=0;i<n;i++)
            {
         printf("%d\t",a[i]);
            }
        }
        break;
        case 2:
        {
            printf("entered elements are ");
            for(int i=0;i<n;i++)
            {
         printf("%d\t",a[i]);
            }
            printf("\nenter location where you want to insert new element ");
            scanf("%d",&l);
            printf("enter value of new element ");
            scanf("%d",&k);
            for(int i=n-1;i>=l-1;i--)
            {
                a[i+1]=a[i];
            }
            a[l-1]=k;
            printf("new array is");
            for(int i=0;i<=n;i++)
            {
         printf("%d\t",a[i]);
            }
        }
        break;
        case 3:
        {
            printf("entered elements are ");
            for(int i=0;i<n;i++)
            {
         printf("%d\t",a[i]);
            }
            printf("\nenter location where you want to delete element ");
            scanf("%d",&l);
            for(int i=l-1;i<n-1;i++)
            {
                a[i]=a[i+1];
            }
            printf("new array is");
            for(int i=0;i<n-1;i++)
            {
         printf("%d\t",a[i]); 
        }
    }
    return 0;
    }
}
