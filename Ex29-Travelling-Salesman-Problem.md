# Ex29 Travelling Salesman Problem
## DATE:
## AIM:
To write a C Program to implement Travelling Salesman Problem for finding shortest path.
## Algorithm
1. Input the number of cities and the distance matrix.
2. Initialize all cities as unvisited.
3. Start from the first city and mark it visited.
4. At each step, select the nearest unvisited city using the least function. 
5. Continue the process until all cities are visited and return to the starting city.
6. Accumulate the total cost of the path.
7. Display the path and the minimum cost.

## Program:
```
/*
Program to implement Travelling Salesman Problem for finding shortest path
Developed by: SWETHA S
RegisterNumber: 212222230155 
*/
```
```
/*
#include<stdio.h>
int a[10][10],visited[10],n,cost=0;

void get()
{
	int i,j;
		scanf("%d",&n);
	for(i=0;i < n;i++)
	{
			for( j=0;j < n;j++)
			scanf("%d",&a[i][j]);
		visited[i]=0;
	}
	}

void mincost(int city)
{
	int ncity;
	int least(int);
	visited[city]=1;	
	printf("%d -->",city+1);
	ncity=least(city);
	if(ncity==999)
	{
		ncity=0;
		printf("%d",ncity+1);
		cost+=a[city][ncity];
		return;
	}
	mincost(ncity);
}

int least(int c)
{
	int i,nc=999;
	int min=999,kmin;
	for(i=0;i < n;i++)
	{
		if((a[c][i]!=0)&&(visited[i]==0))
			if(a[c][i] < min)
			{
				min=a[i][0]+a[c][i];
				kmin=a[c][i];
				nc=i;
			}
	}
	if(min!=999)
		cost+=kmin;
	return nc;
}

void put()
{
	printf("\n\nMinimum cost:%d",cost);
	}

int main()
{
	get();
	mincost(0);
	put();
	return 0;
	}

*/
```
## Output:

<img width="667" height="576" alt="image" src="https://github.com/user-attachments/assets/61372555-9d28-45e4-a1d6-e9a7b6d2992d" />


## Result:
Thus, the C program to implement Travelling Salesman Problem for finding shortest path is implemented successfully.
