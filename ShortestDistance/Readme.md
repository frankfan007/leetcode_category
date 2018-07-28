# Shortest Distance

## Dijkstra's algorithm

The time complexity depends on how to support the operations
* **return the min key** to find the next nearest node (T1 time)
* **decrease some key** to update the distance to the neighbors of the nearest node (T2 time)

The time complexity is: `O(E T2 + V T1)`.

If you use a binary heap or BST, `T1=T2=O(log V)`
Elif you use a Fibonacci heap, `T2=O(1)` and `T1 = O(log V)`.


See <https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm> for algorithm pseudo code 
and <https://en.wikipedia.org/wiki/Binary_heap> for compaison between heap implementations.

But, how to quickly finish the code in interviews? One trick is to skip the decrease key operation and just insert the value directly.
This step would increase the size of the queue from `V` to `E`, but simplify your code. But you should make sure the interviewee knows that you know the Fibonacci implement!!

