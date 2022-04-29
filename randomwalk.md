Grnerating and visualizing data for a random using Python( matplotlib)
### Creating the RandomWalk() Class
random_walk.py
```python
from random import choice

class RandomWalk():
 """A class to generate random walks."""
 
 def __init__(self, num_points=5000):
 """Initialize attributes of a walk."""
 self.num_points = num_points
 
 # All walks start at (0, 0).
 self.x_values = [0]
 self.y_values = [0]
 def fill_walk(self):
"""Calculate all the points in the walk."""
 
 # Keep taking steps until the walk reaches the desired length.
 while len(self.x_values) < self.num_points:
# Decide which direction to go and how far to go in that direction.
 x_direction = choice([1, -1])
 x_distance = choice([0, 1, 2, 3, 4])
 x_step = x_direction * x_distance
 
 y_direction = choice([1, -1])
 y_distance = choice([0, 1, 2, 3, 4])
 y_step = y_direction * y_distance
 
 # Reject moves that go nowhere.
 if x_step == 0 and y_step == 0:
 continue
 
 # Calculate the next x and y values.
 next_x = self.x_values[-1] + x_step
 next_y = self.y_values[-1] + y_step
 
 self.x_values.append(next_x)
 self.y_values.append(next_y)

```
### Plotting ana colouring the Random Walk
rw_visual.py
```python
import matplotlib.pyplot as plt
from random_walk import RandomWalk
# Make a random walk, and plot the points.
rw = RandomWalk()
rw.fill_walk()
point_numbers = list(range(rw.num_points))
plt.scatter(rw.x_values, rw.y_values, c=point_numbers, cmap=plt.cm.Blues,
edgecolor='none', s=15)
plt.scatter(rw.x_values, rw.y_values, s=15)
plt.show()
```
### Adding Plot Points to 50000
```python
import matplotlib.pyplot as plt
from random_walk import RandomWalk
# Make a random walk, and plot the points.
rw = RandomWalk(50000)
rw.fill_walk()
point_numbers = list(range(rw.num_points))
plt.scatter(rw.x_values, rw.y_values, c=point_numbers, cmap=plt.cm.Blues,
 edgecolor='none', s=1)
plt.scatter(rw.x_values, rw.y_values, s=15)
plt.show()
```
