# Ex26 Prim’s Algorithm
## DATE:
## AIM:
To write a C program to implement Prim's Algorithm for finding Total Cost of tree.

## Algorithm
1. Represent the graph as an adjacency matrix G[][].
2. Initialize spanning[][] to store the MST and cost[][] for edge weights.
3. Start from an initial vertex (usually vertex 0), mark it visited, and set distances to adjacent vertices.
4. Repeat the following until all vertices are included in the MST:
Select the unvisited vertex with the minimum distance.
Include it in the MST and update the total cost.
Update distances of vertices adjacent to the newly included vertex if smaller edges are found. 
5. Print the MST matrix and the total cost of the spanning tree.  

## Program:
```
/*
Program to implement Prim's Algorithm
Developed by: SWETHA S
RegisterNumber: 212222230155 
*/
```
```
/*
#include<stdio.h>
#include<stdlib.h>
 
#define infinity 9999
#define MAX 20
 
int G[MAX][MAX],spanning[MAX][MAX],n;
 
int prims();
 
int main()
{
int i,j,total_cost;
scanf("%d",&n);
for(i=0;i<n;i++)
for(j=0;j<n;j++)
scanf("%d",&G[i][j]);
total_cost=prims();

for(i=0;i<n;i++)
{
for(j=0;j<n;j++)
printf("%d ",spanning[i][j]);
printf("\n");
}
printf("\nTotal cost of spanning tree=%d",total_cost);
return 0;
}
 
int prims()
{
int cost[MAX][MAX];
int u,v,min_distance,distance[MAX],from[MAX];
int visited[MAX],no_of_edges,i,min_cost,j;
//create cost[][] matrix,spanning[][]

// Text your code here
for(i=0;i<n;i++)
for(j=0;j<n;j++)
{
    if(G[i][j]==0)
    {
        cost[i][j]=infinity;
    }
    else
    {
        cost[i][j]=G[i][j];
        spanning[i][j]=0;
    }
}

//initialise visited[],distance[] and from[]
distance[0]=0;
visited[0]=1;
for(i=1;i<n;i++)
{
    distance[i]=cost[0][i];
    from[i]=0;
    visited[i]=0;
}
//cost of spanning tree
min_cost=0;
//no. of edges to be added
no_of_edges=n-1;
//initialise visited[],distance[] and from[]
//cost of spanning tree
//no. of edges to be added


while(no_of_edges>0)
{
//find the vertex at minimum distance from the tree
min_distance=infinity;
for(i=1;i<n;i++)
if(visited[i]==0&&distance[i]<min_distance)
{
v=i;
min_distance=distance[i];
}
u=from[v];
//insert the edge in spanning tree
spanning[u][v]=distance[v];
spanning[v][u]=distance[v];
no_of_edges--;
visited[v]=1;
//updated the distance[] array
for(i=1;i<n;i++)
if(visited[i]==0&&cost[i][v]<distance[i])
{
distance[i]=cost[i][v];
from[i]=v;
}
min_cost=min_cost+cost[u][v];
}
return(min_cost);
}
*/
```
## Output:

<img width="790" height="609" alt="image" src="https://github.com/user-attachments/assets/36962f5b-a9bd-4976-a761-bf764e1fb767" />


## Result:
Thus, the C program to implement Prim's Algorithm for finding Total Cost of tree is implemented successfully.
