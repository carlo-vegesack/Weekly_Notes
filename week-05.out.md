# Week 5: Searching and Sorting

Searching and sorting seems like such primitive tasks that everything must have all been said and done about them already, right? Actually not. They are so fundamental that people keep inventing newer and better ways to use them in new and special ways. We can only scratch the surface of them this week, but scratch it we will!

## Exercises

### Binary search

We argued that the worst-case running time for the binary search is $O(\log n)$.

**Exercise:** What is the best-case running time, and what would the input data look like to achieve it?

### Selection sort

**Exercise:** Give an example input where selection sort is not stable.

### Insertion sort

We argued that the worst-case running time for insertion sort was $O(n^2)$ but the best-case running time was $O(n)$.

**Exercise:** Describe what the input data, `numbers`, should look like to actually achieve the worst- and best-case running times.

### Bubble sort

Recall the invariants of the inner ($I$) and outer ($O_n$) loop of bubble sort from the book:

$$I : \forall k \in [0,i-1):x[k] \le x[i-1]$$ 
$$O_1 : \forall k \in [n-j,n-1):x[k] \le x[k+1]$$
$$O_2 : \forall k \in [0,n-j):x[k] \le x[n-j]$$

**Exercise:** Since $O_1$ and $O_2$ tells us that the last j elements are already the largest numbers and are already sorted, we do not need to have the inner loop iterate through these last j elements. How would you exploit this to improve the running time of bubble sort? The worst-case behaviour will not improve, but you can change the running time to about half of the one we have above. Show that this is the case.

**Exercise:** With cocktail sort, after running the outer loop j times, both the first j and the last j elements are in their final positions. Show that this is the case.

**Exercise:** Knowing that both the first and last j elements are already in their right position can be used to iterate over fewer elements in the inner loops. Modify the algorithm to exploit this. The worst case complexity will still be $O(n^2)$, but you will make fewer comparisons. How much do you reduce the number of comparisons by?

### Comparison sort comparison

**Exercise:** Insertion sort runs in $O(n^2)$ when the input is sorted in the reverse order, but can process sorted sequences in $O(n)$. If we can recognise that the input is ordered in reverse, we could first reverse the sequence and then run the insertion sort. Show that we can reverse a sequence, in place, in $O(n)$. Try to adapt insertion sort, so you first recognise consecutive runs of non-increasing elements, then reverse these before you run insertion sort on the result. Show that the worst-case running time is still $O(n^2)$, but try to compare the modified algorithm with the traditional insertion sort to see if it works better in practice.

### Bucket sort

**Exercise:** Argue why the inner loop in

```python
result_keys, result_values = [], []
for key in range(m):
 for val in buckets[key]:
  result_keys.append(key) #This line
  result_values.append(val) #And this line
```

only executes n times.

**Exercise:** Argue why the bucket sort actually sorts the input.

If you want to see a more efficient, and more traditional, bucket sort, then try [this exercise][w05-bucket-ex].


[command-line-ex]: https://github.com/birc-ctib/command-lines-and-pipes
[intro-to-github-ex]: https://github.com/birc-ctib/intro-to-git-and-github

[w02-prog-ex]: https://github.com/birc-ctib/basic-python
[w02-commandline-ex]: https://github.com/birc-ctib/command-line-python

[w03-merge-ex]: https://github.com/birc-ctib/merging
[w03-guessing-ex]: https://github.com/birc-ctib/guessing
[w03-base-ex]: https://github.com/birc-ctib/changing-base
[w03-sieve-ex]: https://github.com/birc-ctib/sieve
[w03-substring-ex]: https://github.com/birc-ctib/lis
[w03-powerset-ex]: https://github.com/birc-ctib/powerset
[w03-subseq-ex]: https://github.com/birc-ctib/liseq

[w05-bucket-ex]: https://github.com/birc-ctib/bucket-sort

[w06-simple-funcs-ex]: https://github.com/birc-ctib/simple-funcs
[w06-kmers-ex]: https://github.com/birc-ctib/kmer
[w06-reduce-ex]: https://github.com/birc-ctib/reduce

[w07-lists-ex]: https://github.com/birc-ctib/lists-and-recursion

[w09-mm-ex]: https://github.com/birc-ctib/markov

[w11-sllists-ex]: https://github.com/birc-ctib/singly-linked-lists
[w11-dllists-ex]: https://github.com/birc-ctib/doubly-linked-lists

[w12-list-set-ex]: https://github.com/birc-ctib/list-set
[w12-search-tree-set-ex]: https://github.com/birc-ctib/st-balance-1
[w12-hash-table-ex]: https://github.com/birc-ctib/hash-set

[w13-linked-list-stack-ex]: https://github.com/birc-ctib/linked-list-stack
[w13-newick-ex]: https://github.com/birc-ctib/newick
[w13-dllist-queue-ex]: https://github.com/birc-ctib/linked-list-queue

[w14-huffmann-ex]: https://github.com/birc-ctib/huffman
[w14-prim-ex]: https://github.com/birc-ctib/prim
[w14-search-tree-pqueue-ex]: https://github.com/birc-ctib/st-pqueue
[w14-leftist-heap-ex]: https://github.com/birc-ctib/leftist
[w14-binary-heap-ex]: https://github.com/birc-ctib/binary-heap
[w14-heap-sort-ex]: https://github.com/birc-ctib/heap-sort



