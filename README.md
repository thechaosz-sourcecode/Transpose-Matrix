Transpose-Matrix
================

Here here here.. Let’s discuss again about C++ programming language and topic is Transpose Matrix.

In math, we’ve learned about matrix and how to add two matrix, even for times, divide, and transpose matrix. I have a friend who just started his university life as a computer science major and asked me about how to write transpose matrix using C or C++ language. It sounds so easy for us who already trained well, but for someone who just be in touch on programming world gonna be confused and as his demand, I’ll share my simple code of C++ here !

Note  : click here if you don’t know about transpose matrix.

#include <cstdio>
#include <iostream>

using namespace std;

int main()
{
int row,column,c,d;
int transpose[20][20];
int matrix[20][20];

cout <<"Input how many rows and column of a matrix (separated by a space): " <<endl;
cin >> row >> column ;
cout <<endl;
cout <<"Input your matrix value (rows separated by a space and coloumns with enter ) : " <<endl;

for (int i=0; i < row; i++) //input your value to the matrix array
{
     for (int j=0; j<column;j++)
    {
      cin >> matrix[i][j];
    }
}

//------processing is here-------------
for (int i=0; i < row; i++)
{
     for (int j=0; j<column;j++)
    {
     transpose[j][i] = matrix [i][j];
    }
}

cout<<endl<<"The result of Tranpose Matrix : "<<endl;
for (int i=0; i < column; i++) //print out your result
{
    for (int j=0; j<row;j++)
    {
     cout<<transpose[i][j]<<"\t";
    }
     cout<<endl;
}

system("pause");
return 0;
}
Explain:
for (int i=0; i < row; i++) //input your value to the matrix array
{
     for (int j=0; j<column;j++)
    {
      cin >> matrix[i][j];
    }
}
In this section,major usage of 2 for-loop is because our matrix is 2D. and input the value one by one inside the array of ‘matrix’ and firstly, we input columns value in the first row and after finished,i will be go to second row and go on.

 

for (int i=0; i < row; i++)
{
     for (int j=0; j<column;j++)
    {
     transpose[j][i] = matrix [i][j];
    }
}
}
it’s simple here, because in transpose matrix we need to change row becomes column and column becomes row, so just change the array’s place.

 

for (int i=0; i < column; i++) //print out your result
{
    for (int j=0; j<row;j++)
    {
     cout<<transpose[i][j]<<"\t";
    }
     cout<<endl;
}
}
In for-loop here, you need to change it from column first then row. It because after transposed the matrix, your third column from transpose’s variable already NULL and it will print out the memory address.

Download our code at github here.

Hope you got it well and have fun with your program! 
