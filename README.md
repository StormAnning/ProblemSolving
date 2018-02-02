
Primitive Types
-	Be comfortable with bitwise operators XOR..
-	Use masks on bits
-	Understand signedness and implications of shifting
-	Consider caching bit values, e.g. we pre-compute partitys..
-	Be aware of commutativity and associativity can be used to perform stuff in parallel
Arrays
-	Often have simple brute force solutions that use O(n) space
-	Filling from front is slow - so try to fill from the back
-	Instead of deleting an entry that requires shifting -> overwrite it- or swap with last, and delete!
-	Consider processing from the back of the array for integers
Strings
-	Often have simple brute force solutions that use O(n) space
-	Updating string from the front is slow - so write form the back
Linked-Lists
-	Simple brute force solutions that have O(n) space
-	Use a dummy head 
-	Often benefits from using slow/fast pointers.
-	Merge-Sort effective in merging two lists, often able to do things in place.
Stacks-Queues
-	Parsing benefits from stack
-	Consider augmenting the stack for additional operations such as find max, or other data.
-	Useful for merging items! Intervals - CandyCrush etc! Merging last seen values with new values. Great for stuff that requires a look ahead!
Binary Trees
-	Recursive algorithms are well suited to problems on trees
-	Often have simple O(n) space brute force solutions
-	Consider skewed trees, height of O(h) not always O(lg(n))
-	Often useful to use Queues to process elements in levels/manipulate the tree.
-	If has parent node can make it simple
Heaps
-	PQ use if all you care about is max and min element
-	Don’t need to support fast search, delete, insert etc.
-	Compute the k-largest (use min heap) or k-smallest element (use max heap) (use two for median)
Searching
-	Binary search - finding elements, approximating stuff
-	If your solution does not require sorting look for solutions that don’t require the full sort. (Partition) DutchFlagParition
-	Consider time/space trade offs/ and making multiple passes through the array
Hash Tables
-	Fast insert, lookup only O(n) if needs to be resized / load factor sucks
-	Use to enhance other algorithms!
-	Good for precomputation!
-	Be wary of hashing an object that it is hashed on the correct properties - so two equal things actually match
Sorting
-	Use to make steps in an algorithm faster
-	Think if sorting makes finding a solution easier? - What intuitions result?
-	Sorting may allows us to eliminate values and stick to some INVARIANT.
-	For small values - Counting sort - O(n), Bucket Sort... all others O(nlg(n))
-	Not always obvious what to sort on, start points or end points?
Binary Search Tree
-	Use hash table to get additional O(1) lookup
-	Think about augmenting it, e.g. adding heights and depths to calculate certain aspects.
-	Think of the global property of BSTS (child < >)
-	Use recursion etc to manipulate - solve sub-tree problems.
Recursion
-	Decompose problem into smaller sub problem of the same type that converges into a sub problem you know how to solve. Then Let the RECURSION FAIRY handle it!
-	Suitable when input expressed using recursive rules
-	Good for search, enumeration, and divide and conquer
-	Alternative to deeply nested iteration
-	Tail recursion can easily be converted to a do while loop
-	If you need to make a recursive function iterative consider using a stack
-	Cache results - DP
BackTracking
-	Back off from results that didn’t pan out DFS.
-	Can often greatly prune results by being smart by where to initially search e.g. sudoku, pick cells with already populate neighbours - greatly reduce the number of calls.
Dynamic Programming
-	When OVERLAPPING subproblems / Optimal Sub-Structures
-	Counting or Optimization problems
-	Search Problems
-	Top Down or Bottom up - Forward or Backward
-	Figure out the sub-problems -> problems of the same type as the original but smaller.
-	Identify the cases
-	Identify how sub problems depend on previous problems
-	Figure out base case problems that you can easily solve.
Write a recurrence relation.
-	Find evaluation order.. DAG etc.
-	Use two arrays? Or Multiple DP problems into one - MIN-MAX etc.
Greedy/Invariants
-	Local Optimum choices at each step that lead to global
-	Never unmake a choice
-	Scan both ways? Etc…
-	Only ever depends on one optima sub-problem!!!
Graphs
-	Use when need to work out calculated objects
-	Good for analysing relationships
-	DFS - WONT FIND SHORTEST PATH
-	BFS - will on non weighted
-	Dijkstra - will on weighted
-	Floyd Warshall - shortest paths on all, negative weights.
