# CI2024_lab02


### Fast algorithm

- **Greedy Initialization**:
Start with greedy algorithm, picking a starting city and always go to the nearest unvisited city until I've visited all of them.

- **Simulated Annealing**:
Take my initial route and try to improve it by looking for nearby routes that might be better. If a route that’s shorter, I take it. But if it’s longer, I still might accept it based on a probability that decreases over time, helping avoiding getting stuck in a local optimum.
I keep doing this until I reach a point where the temperature (or probability of accepting worse solutions) is really low, meaning that we are in a "good" solution.

- **Inversion Mutation**:
Within the simulated annealing process, I implement inversion mutation. This is where I randomly choose a segment of my route (at least 4 cities) and reverse the order of those cities. This increases chances of finding a better route that the initial greedy algorithm might have overlooked.

- **Overall result**
I get in general a cost of 4320.24534825164 and 5055 steps (depends on the randomnesses)



### Slower algorithm 

- **Greedy Initialization**:
Same as before

- **Parent Selection**:
Valid parents for the next generation are selected based on their fitness scores (involving to randomly choosing two candidates from the population and sorting them by fitness).

- **Crossover Operation**:
I use a two-point crossover technique to create offspring from selected parent individuals.

- **Mutation**:
Contains 2 opérations : inversion mutation as before and also a random 50% swap of two cities to try other options

- **Overall result**:
I get in general a cost of 4260.041049398426 and 40011 steps, much more steps but a better cost (still not optimal)