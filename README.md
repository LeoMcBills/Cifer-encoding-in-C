//Cifer-encoding-in-C

#include<stdio.h>
#include<string.h>
main()
{
//Converting ascii values to binary including space and everything
int i,temp,x,y=1,binary=0;
 char str[1000];
 printf("Enter a sentence\n");
 gets(str);
 i=0;
 printf("Encrypted Binary code\n");
  while(str[i]!='\0')
  {
      y=1,binary=0;
      temp=str[i];
      while(temp!=0)
       {
         x=temp%2;
         binary=binary+(x*y);
         temp=temp/2;
         y=y*10;
        }
        printf("%d ",binary);

   i++;
  }
  printf("\n");
}
