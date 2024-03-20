# Problem Statement

## Fly me to my destination - It's urgent!!

Consider there are **N** airports in the world, each airport has a plane available with limited units of fuel available to fly. 

You are initially positioned at airport **number one** and you have to reach the last airport (**N**) by hiring a **minimum** number of planes. You'd need 1 unit of fuel to fly to the nearest airport from any airport. 

You will be given an array of N numbers each representing the units of fuel available in the plane at that particular airport. Print the number of planes you'd need to hire to reach the last airport. If it is not possible to reach the last airport, return -1

Example: 

Array = [2,1,2,3,1]

In the given array, there are 5 airports, the plane at the starting airport has 2 units of fuel so you can hire this plane and stop at the 2nd or 3rd airport. The plane at the 2nd airport has 1 unit of fuel so it can fly to the 3rd airport only. The minimum number of planes required in this case is two 2 → 2→ 1. 

Example 2:

Array = [1,6,3,4,5,0,0,0,6]

In the given array, there are 9 airports, the plane at the starting airport has 1 unit of fuel, so you can hire this plane and stop at the 2nd airport only. The plane at the 2nd airport has 6 units of fuel, so it can fly to the 3rd, 4th, 5th, 6th, 7th, or 8th airport. If we take the plane at the 5th airport, the minimum number of planes required in this case is three 1 → 6 → 5 → 6


## Solution


**Code Explanation:**
1. **Function Declaration:** 
   The code starts with declaring a function named `minimumRequiredPlanes`, which takes an array of numbers as input.

2. **Initializing `Requiredplanes` Array:**
   Inside the function, a new array called `Requiredplanes` is created. This array will keep track of the minimum number of planes required to reach each airport. Initially, all elements of this array are set to a very large number to indicate that the number of planes required to reach any airport hasn't been calculated yet.

3. **Setting Initial Condition:**
   The first airport (index 0) is set to a minimum plane count of 0, indicating that it can be reached without needing any planes.

4. **Algorithm Execution:**
   The code then enters a loop to iterate over each airport in the array. Within this loop, there's another nested loop that checks all possible paths from the current airport (`i`) to other airports (`j`). It updates the `planesRequired` array with the minimum number of planes required to reach each airport.

5. **Final Result:**
   After completing the iterations, the function checks if it's possible to reach the last airport. If it's possible, it returns the minimum number of planes required to reach the last airport. If not, it returns -1, indicating that it's impossible to reach the last airport.

**Algorithm Explanation:**
1. **Initialization:**
   We start by setting up a placeholder for each airport to keep track of the minimum number of planes required to reach them. Initially, we don't know how many planes are needed, so we use a large number to represent this uncertainty.

2. **Starting Point:**
   We know that the first airport can be reached without any planes, so we set its minimum plane count to 0.

3. **Iterating Through Airports:**
   We go through each airport in the array and consider all possible paths from the current airport to other airports. For each path, we update the minimum plane count required to reach that airport if it's less than the previously calculated count.

4. **Finding the Solution:**
   After considering all paths, we check if it's possible to reach the last airport. If it is, we return the minimum number of planes required to reach it. If not, we conclude that it's impossible to reach the last airport.

5. **Output:**
   Finally, we get the output - the minimum number of planes required to reach the last airport based on the given array of distances between airports.

In simpler terms, the algorithm figures out the minimum number of planes needed to travel from the first airport to the last airport considering the distances between them.
