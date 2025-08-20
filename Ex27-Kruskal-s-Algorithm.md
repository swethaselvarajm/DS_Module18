# Ex27 Kruskal’s Algorithm
## DATE:
## AIM:
To write a C program to implement Kruskal's Algorithm for finding minimum cost

## Algorithm
1. Represent the graph using a cost adjacency matrix. Replace 0 (no edge) with a large value like 999 to indicate infinity.
2. Initialize the parent array for union-find operations.
3. Repeat until n-1 edges are selected:
Find the edge with the minimum cost from the remaining edges.
Use the find() function to check if including this edge forms a cycle.
If it does not form a cycle, include the edge in the MST and update total cost.
Mark the edge as used by setting its cost to infinity (999).
4. Print all edges included in the MST and the total minimum cost.
  

## Program:
```
/*
Program to implement Kruskal's Algorithm
Developed by: SWETHA S
RegisterNumber: 212222230155
*/
```
```
/*
    #include <stdio.h>
    #include <stdlib.h>
    int i,j,k,a,b,u,v,n,ne=1;
    int min,mincost=0,cost[9][9],parent[9];
    int find(int);
    int uni(int,int);
    int main()
    {
          scanf("%d",&n);
          for(i=1;i<=n;i++)
     {
     for(j=1;j<=n;j++)
     {
     scanf("%d",&cost[i][j]);
     if(cost[i][j]==0)
     cost[i][j]=999;
     }
     }
         while(ne < n)
     {
     for(i=1,min=999;i<=n;i++)
     {
     for(j=1;j <= n;j++)
     {
    
    // Text your code here
    if(cost[i][j]<min)
    {
        min=cost[i][j];
        a=u=i;
        b=v=j;
    }
     }
     }
    u=find(u);
    v=find(v);
    if(uni(u,v))
    {
        printf("%d edge (%d,%d) =%d\n",ne++,a,b,min);
        mincost+=min;
    }
    
    
    
     cost[a][b]=cost[b][a]=999;
     }
     printf("Minimum cost = %d\n",mincost);
     return 0;
       }
    int find(int i)
    {
     while(parent[i])
     i=parent[i];
     return i;
    }
    int uni(int i,int j)
    {
     if(i!=j)
     {
     parent[j]=i;
     return 1;
     }
     return 0;
    }
*/
```
## Output:

<img width="493" height="467" alt="image" src="https://github.com/user-attachments/assets/6e1a9f44-4d66-412b-a625-dbbb0aef33ce" />


## Result:
Thus, the C program to implement Kruskal's Algorithm for finding minimum cost is implemented successfully.
