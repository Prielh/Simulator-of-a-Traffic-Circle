# Simulator-of-a-Traffic-Circle
Simulator of a traffic circle that help predict congestion in a junction.
The traffic circle in this case is actually described as squares that together make up a large square (which is the traffic circle) so that each square can contain up to one car. In other words, every such square must be mutually exclusive.
At each corner of the large square there are four car generators. Each of them generates a new car once in a randomized time according to a certain range. 
A car will be able to enter the traffic circle under two conditions:
1) A car that has been generated enters the circle only once the square to which it wants to enter.
2) The square before it are free.

A car will try to move to the next square every INTER_MOVES_IN_NS. If the next square is free, the car moves there. Otherwise, it will wait until the square is free.
In addition, there are 4 exit points at the corners of the circle so that any car can leave the circle through them with probability FIN_PROB. A car will only be able to exit the circle if he has passed at least one side of the square.
During the simulation, a snapshot of the location of the cars in the circle will be printed on the screen 10 times.
