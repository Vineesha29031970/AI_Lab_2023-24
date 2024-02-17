# Ex.No: 1  Implementation of Breadth First Search 
### DATE: 17/02/2024                                                                            
### REGISTER NUMBER : 212221040180
### AIM: 
To write a python program to implement Breadth first Search. 
### Algorithm:
1. Start the program
2. Create the graph by using adjacency list representation
3. Define a function bfs and take the set “visited” is empty and “queue” is empty
4. Search start with initial node and add the node to visited and queue.
5. For each neighbor node, check node is not in visited then add node to visited and queue list.
6.  Creating loop to print the visited node.
7.   Call the bfs function by passing arguments visited, graph and starting node.
8.   Stop the program.
   
### Program:

'''

graph = {
  '2': ['3', '4'],
  '3': ['5'],
  '4': ['6', '7'],
  '6': [],
  '5': ['6'],
  '7': ['8'],
  '8': []
}

visited = []  # List for visited nodes.
queue = []    # Initialize a queue

def bfs(visited, graph, node):  # Function for BFS
    visited.append(node)
    queue.append(node)

    while queue:  # Creating loop to visit each node
        m = queue.pop(0)
        print(m, end=" ")

        for neighbour in graph[m]:
            if neighbour not in visited:
                visited.append(neighbour)
                queue.append(neighbour)

# Driver Code
print("BFS order is")
bfs(visited, graph, '2')

'''



### Output:

<img width="753" alt="image" src="https://github.com/Vineesha29031970/AI_Lab_2023-24/assets/133136880/d1e49938-e353-4a7f-9a3a-47c6fd06a7e1">


### Result:
Thus the breadth first search order was found sucessfully.
