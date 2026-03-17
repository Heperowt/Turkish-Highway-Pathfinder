# 🛣️ Turkish Highway Pathfinder & Distance Analyzer

![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white)
![.NET](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white)

A comprehensive C# console application developed to model the highway connections between all 81 provinces of Türkiye. This project demonstrates the practical application of **Data Structures (Graphs & Dictionaries)**, **Matrices**, and **Search Algorithms (Greedy)** to solve geographical pathfinding problems.

## 📋 Project Requirements (A to H)
The source code contains comments (e.g., `//a:`, `//c:`) that correspond to the specific requirements of this assignment. Here is the mapping:
* **a) Distance Matrix:** Create an 81x81 matrix storing the highway distances between all 81 provinces using the official KGM distance table.
* **b) City Names Array:** Store the names of the 81 provinces in an array, indexed by their official license plate numbers.
* **c) Random Journey:** Start from a random city and travel to 9 other random cities consecutively. Print the distance of each leg and calculate the total journey distance.
* **d) Neighborhood Graph:** Research the neighboring cities for all 81 provinces and store them in an efficient composite data structure (implemented as a `Dictionary<string, List<string>>`). Print the list of all cities and their neighbors.
* **e) Farthest Neighbors:** Traverse the graph data structure to find and print the pair of neighboring cities that have the longest highway distance between them.
* **f) AI Integration (Heuristic Data):** Use Generative AI to obtain a list of the straight-line (bird's-eye) distances from all 81 provinces to Izmir.
* **g) Greedy Path to Izmir:** Select a random starting city. Find a path to Izmir by constantly moving to the neighboring city that has the shortest straight-line distance to Izmir. Calculate the total actual highway distance of this path.
* **h) Algorithmic Analysis:** Explain whether this Greedy approach guarantees the shortest path, compare it with Dijkstra's algorithm, and explain the A* (A-Star) algorithm.

## 🚀 Key Features & Implementation
- **Distance Matrix & Mapping:** Constructs an 81x81 matrix and maps them to respective province names.
- **Random Journey Simulation:** Generates a random valid route spanning 10 distinct cities.
- **Graph Data Structure:** Parses neighborhood data and builds a robust Graph representation.
- **Greedy Pathfinding to Izmir:** Utilizes AI-generated heuristic data and makes locally optimal choices to navigate to the destination.

## 🧠 Algorithmic Analysis: Greedy vs. Dijkstra & A-Star
The **Greedy Algorithm** used in this application does not guarantee the absolute shortest actual highway path. It strictly relies on a heuristic (the estimated straight-line distance to Izmir) and ignores the accumulated travel cost of the roads taken. 
- **Advantage:** It is significantly faster and less memory-intensive than **Dijkstra's Algorithm**.
- **Alternative (A-Star):** By combining Dijkstra's method of tracking actual distance traveled with the Greedy algorithm's heuristic function, the **A-Star (A*)** algorithm provides the optimal balance—yielding both computational speed and the guaranteed shortest path.

## 🛠️ How to Run
1. Clone the repository.
2. Open the project in Visual Studio or any IDE supporting C# .NET.
3. Build and Run the `Program.cs` file.
