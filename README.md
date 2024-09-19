code of insertion deletion transitive

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













code number 2 linear binary search using switch case



#include <stdio.h>

int main()
{
    int ch;
    
    printf("Enter the number for the search to be performed:\n 1. linear search \n 2. binary search\n");
    scanf("%d",&ch);
    switch(ch)
    {
      case 1:
      {
        int a[100], s, i, n;

        printf("Enter number of elements in array\n");
        scanf("%d", &n);

  
        printf("Enter elements in array\n");

          for (i = 0; i < n; i++)
          {
          scanf("%d", &a[i]);
          }

          printf("Enter a number to search\n");
          scanf("%d", &s);
          for (i = 0; i < n; i++)
        {
         if (a[i] == s)  
      {
          printf("%d is present at location %d.\n", s, i+1);
        break;
       }
       }
        if (i == n)
        printf("%d not present in the array.\n", s);
          
         break;  
      }
      
      case 2:
      {
        
       int i, first, last, middle, n, s, a[100];

        printf("Enter number of elements\n");
        scanf("%d", &n);

        printf("Enter %d numbers\n", n);

        for (i = 0; i < n; i++)
     scanf("%d", &a[i]);

      printf("Enter number to find\n");
     scanf("%d", &s);

       first = 0;
       last = n - 1;
       middle = (first+last)/2;

      while (first <= last) 
      {
      if (a[middle] < s)
      first = middle + 1;
      else if (a[middle]==s)
      {
      printf("%d found at location %d.\n", s, middle+1);
      break;
     }
     else
      last = middle - 1;

     middle = (first + last)/2;
     }
     if (first > last)
     printf("Not found! %d isn't present in the list.\n", s);
       break; 
      }
      default:
      printf("\n Invalid input");
      break;
    }

    return 0;
}
