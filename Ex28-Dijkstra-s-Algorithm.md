# Ex28 Dijkstra’s Algorithm
## DATE:
## AIM:
To write a C Program to implement Dijkstra's Algorithm to find the shortest path

## Algorithm
1. Represent the graph using an adjacency matrix; replace 0 (no edge) with a large number (INFINITY).
2. Initialize arrays:
distance[] to store shortest distance from the source.
pred[] to store predecessors of nodes for path reconstruction.
visited[] to track visited nodes.
3. Set the distance of the start node to 0 and mark it visited.
4. For all unvisited nodes, select the node with the smallest distance and mark it visited. 
5. Update the distance of neighboring nodes if a shorter path exists via the selected node.  

## Program:
```
/*
Program to implement Dijkstra's Algorithm 
Developed by: SWETHA S
RegisterNumber: 212222230155 
*/
```
```
/*
#include<stdio.h>
#define INFINITY 9999
#define MAX 10
 
void dijkstra(int G[MAX][MAX],int n,int startnode);
 
int main()
{
int G[MAX][MAX],i,j,n,u;
scanf("%d",&n);
for(i=0;i<n;i++)
for(j=0;j<n;j++)
scanf("%d",&G[i][j]);
scanf("%d",&u);
dijkstra(G,n,u);
return 0;
}
 
void dijkstra(int G[MAX][MAX],int n,int startnode)
{
 
int cost[MAX][MAX],distance[MAX],pred[MAX];
int visited[MAX],count,mindistance,nextnode,i,j;
//pred[] stores the predecessor of each node
//count gives the number of nodes seen so far
//create the cost matrix
for(i=0;i<n;i++)
for(j=0;j<n;j++)
if(G[i][j]==0)
cost[i][j]=INFINITY;
else
cost[i][j]=G[i][j];
//initialize pred[],distance[] and visited[]
for(i=0;i<n;i++)
{
distance[i]=cost[startnode][i];
pred[i]=startnode;
visited[i]=0;
}
distance[startnode]=0;
visited[startnode]=1;
count=1;
while(count<n-1)
{
mindistance=INFINITY;
//nextnode gives the node at minimum distance
for(i=0;i<n;i++)
if(distance[i]<mindistance&&!visited[i])
{
mindistance=distance[i];
nextnode=i;
}
//check if a better path exists through nextnode
visited[nextnode]=1;
for(i=0;i<n;i++)
if(!visited[i])
if(mindistance+cost[nextnode][i]<distance[i])
{
distance[i]=mindistance+cost[nextnode][i];
pred[i]=nextnode;
}
count++;
}
 
//print the path and distance of each node

// Text your code here
for(i=0;i<n;i++)
if(i!=startnode)
{
    printf("Distance of node%d=%d\n",i,distance[i]);
    printf("Path=%d",i);
    j=i;
    do{
        j=pred[j];
        printf("<-%d",j);
    }while(j!=startnode);
}


}
*/
```
## Output:

<img width="793" height="602" alt="image" src="https://github.com/user-attachments/assets/93a1b897-76fd-4893-a12c-7522f79d6cd0" />


## Result:
Thus, the Program to implement Dijkstra's Algorithm to find the shortest path is implemented successfully.
