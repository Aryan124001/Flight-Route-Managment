# Flight Route Management System

This repository contains a C++ program to simulate a flight route management system. The system allows users to find the shortest path between two cities based on cost, display all possible routes, and search for paths with a limited number of stops.

## Features

* **Add Routes:** Add flight routes between cities with associated costs.
* **Find Shortest Path:** Compute the shortest path between two cities using Dijkstra's algorithm.
* **Display All Routes:** List all possible routes between two cities.
* **Find Path with Limited Stops:** Search for routes between two cities with a user-defined maximum number of stops.

## Cities Included

The system includes the following cities and their connections:

* Delhi, Mumbai, Bangalore, Hyderabad, Chennai, Kolkata, Ahmedabad, Jaipur, Lucknow, Varanasi, Patna, Ranchi, Bhubaneswar, Pune, Coimbatore.

## Technologies Used

* **Programming Language:** C++
* **Algorithms:** Dijkstra's Algorithm, Depth-First Search (DFS)

## How to Run

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Aryan124001/Flight-Route-Management-System.git
   cd Flight-Route-Management-System
   ```
2. **Compile the Program:**

   ```bash
   g++ -o flight_routes Main.cpp
   ```
3. **Run the Executable:**

   ```bash
   ./flight_routes
   ```

## Usage

1. **Run the program** by compiling the `Main.cpp` file.
2. **Input the starting and destination cities** when prompted.
3. **Select an option** from the menu:

   * **Find Shortest Path:** Displays the shortest path and its cost.
   * **Display All Routes:** Lists all possible routes between the two cities.
   * **Find Path with K Stops:** Finds the cheapest path between two cities with a user-defined maximum number of stops.

## Code Overview

### `FlightRoutes` Class

The program uses the `FlightRoutes` class to manage a graph of cities and their connections.

#### 1. Graph Representation

* A `map<string, vector<pair<string, int>>>` is used to represent the graph:

  * **Key:** City name (case-insensitive)
  * **Value:** A list of pairs containing a connected city and the travel cost

#### 2. Key Functions

* `addRoute`: Adds a bi-directional route between two cities with a given cost.
* `findShortestPath`: Uses Dijkstra's Algorithm to compute the shortest path and cost.
* `displayRoutes`: Uses DFS to find and display all possible routes between two cities.
* `findPathWithKStops`: Finds the cheapest path between two cities with at most K stops.

#### 3. Error Handling

* Detects invalid city names and displays appropriate messages.
* Handles cases where no routes are available.

### Algorithms Used

* **Dijkstra's Algorithm:** Calculates the shortest path in a weighted graph efficiently.
* **Depth-First Search (DFS):** Recursively explores all possible routes between two cities.

## Example Interaction

```plaintext
--- Flight Route Management System ---
List of cities: Delhi, Mumbai, Bangalore, Hyderabad, Chennai, Kolkata, Ahmedabad, Jaipur, Lucknow, Varanasi, Patna, Ranchi, Bhubaneswar, Pune, Coimbatore

Enter starting city: Delhi
Enter destination city: Mumbai

1. Find Shortest Path
2. Display All Routes
3. Find Path with K Stops
Enter your choice:
```
