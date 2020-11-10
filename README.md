
# Matrix-Multiplication-
#include<stdio.h>    
#include<stdlib.h>  
int main(){  
int a[10][10],b[10][10],mul[10][10],r,c,i,j,k;    
system("cls");  
printf("enter the number of row=");    
scanf("%d",&r);    
printf("enter the number of column=");    
scanf("%d",&c);    
printf("enter the first matrix element=\n");    
for(i=0;i<r;i++)    
{    
for(j=0;j<c;j++)    
{    
scanf("%d",&a[i][j]);    
}    
}    
printf("enter the second matrix element=\n");    
for(i=0;i<r;i++)    
{    
for(j=0;j<c;j++)    
{    
scanf("%d",&b[i][j]);    
}    
}    
    
printf("multiply of the matrix=\n");    
for(i=0;i<r;i++)    
{    
for(j=0;j<c;j++)    
{    
mul[i][j]=0;    
for(k=0;k<c;k++)    
{    
mul[i][j]+=a[i][k]*b[k][j];    
}    
}    
}    
//for printing result    
for(i=0;i<r;i++)    
{    
for(j=0;j<c;j++)    
{    
printf("%d\t",mul[i][j]);    
}    
printf("\n");    
}    
return 0;  


######################################################

##### Adding code for subtraction ####}
#include <stdio.h>
#define N 3
// This function subtracts MAT2[][] from MAT1[][], and stores
// the result in RESULT[][]
void subtract(int MAT1[][N], int MAT2[][N], int RESULT[][N]) {
   int i, j;
   for (i = 0; i < N; i++)
   for (j = 0; j < N; j++)
   RESULT[i][j] = MAT1[i][j] - MAT2[i][j];
}
int main() {
   int MAT1[N][N] = { {1, 2, 3},
      {4, 5, 6},
      {7, 8, 9}
      };
   int MAT2[N][N] = { {9, 8, 7},
      {6, 5, 4},
      {3, 2, 1}
   };
   int RESULT[N][N]; // To store result
   int i, j;
   subtract(MAT1, MAT2, RESULT);
   printf("Resultant matrix is \n");
   for (i = 0; i < N; i++) {
      for (j = 0; j < N; j++)
      printf("%d ", RESULT[i][j]);
      printf("\n");
   }
   return 0;
}

END  
