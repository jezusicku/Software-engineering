# p2

#include <iostream>
#include <time.h>
using namespace std;

//losowe liczby
int *arrayy(int n)
{
   srand( time( NULL ) );
	int *arr = new int[n];
	for(int i=0; i<n; i++)
	{
		*(arr+i)=rand()%11;
	}
	return arr;
}

//mnozenie wielomianow
	
	int* mnozenie(int *arr4, int *arr5, int n, int m)
	{
    int *wynik=new int [m+n];
    
    for(int i=0; i<m; i++)
    {
        for(int j=0; j<n; j++)
        {
            *(wynik+i+j)+=*(arr4+i)* *(arr5+j);
        }
    }
    return wynik;
}

//sortowanie

void quick_sort(int *tab, int lewy, int prawy)
{
	if(prawy <= lewy) return;
	
	int i = lewy - 1, j = prawy + 1, 
	pivot = tab[(lewy+prawy)/2]; 
	
	while(1)
	{
		while(pivot>tab[++i]);
		while(pivot<tab[--j]);
		if( i <= j)
			swap(tab[i],tab[j]);
		else
			break;
	}

	if(j > lewy)
	quick_sort(tab, lewy, j);
	if(i < prawy)
	quick_sort(tab, i, prawy);
}


int main()
{
	int n=10;
	int *arr=arrayy(n);
    
	for(int i=0; i<n;i++)
	{
		cout << *(arr+i)<<' ';
	}
    cout << endl;

//najwieksza liczba
    int *ptr1, *ptr2;
    ptr1 = arr;
    ptr2 = arr;
    int max=-2147483646;
    int min=2147483646;

    for(int i=0;i<n;i++)
    {
      if(max <= *ptr1)
      {

     max = *ptr1;

     }

     ptr1++;

   }

    //int *arr2=arrayy(n);
//odwracanie tablicy
    for(int i=0; i<n; i++)
    {
        *(arr2+i)=*(arr+n-i);
    }

    for(int i=0; i<n;i++)
	{
		cout << *(arr+i)<<' ';
	}
    cout <<endl;

//przesuniecie o m pol
int *arr3=arrayy(n);
int m=3;
for(int i=0; i<n; i++)
{
    *(arr3+i)=*(arr+(i+m)%n);
}
for(int i=0; i<n;i++)
	{
		cout << *(arr3+i)<<' ';
	}
//mnozenie wielomianow
int m=8;
    int *arr4=arrayy(n);
    int *arr5=arrayy(m);
    int *wynik=arrayy(m+n);
    wynik=mnozenie(arr4,arr5,n,m);
    for(int i=0; i<n+m; i++)
    {
        cout<<*(wynik+i);
    }
    
//laczenie tablic
   int *arr8=arrayy(n);
   int *arr9=arrayy(n);
   quick_sort(arr8,0,10);
   quick_sort(arr9,0,10);
   int *arr10=new int [20];
   int temp=0;
   int i=0;
   int j=0;
   
   while(temp<n+n)
   {
       
       if(*(arr8+i)<=*(arr9+j))
       {
           *(arr10+temp)=*(arr8+i);
            i++;
            temp++;
       }
       else
       {
           *(arr10+temp)=*(arr9+j);
            j++;
            temp++;
       }
   }
    
    

	return 0;
}




