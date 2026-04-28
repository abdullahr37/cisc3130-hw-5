# Homework 5

For this homework, I implemented two different queue data structures and then used a queue-based approach to do radix sort on non-negative integers.

The first queue I made was `HW5ArrayQueue<T>`. This one uses a circular array. I kept track of the front of the queue and the current size, and when I add a new item I calculate where the rear should go. If the array gets full, I make a new bigger array and copy the items over in the correct order. I used `enqueue()` to add items, `dequeue()` to remove items, and `peek()` to look at the front item without removing it.

The second queue I made was `HW5LinkedQueue<T>`. This version uses linked nodes instead of an array. I kept references to both the front and rear nodes so that adding to the back and removing from the front would be simple. I also kept track of the size of the queue.

After that, I implemented radix sort in `HW5RadixSort`. My radix sort works only for non-negative integers, which is what the assignment asked for. I used 10 queues as buckets for the digits `0` through `9`. For each digit place like ones, tens, and hundreds, I put each number into the correct queue based on that digit. Then I took the numbers back out of the queues in order and put them back into the array. Repeating this for each digit place sorts the array.

I also made `HW5Main` to test my code. In that file, I tested both queue implementations by adding and removing a few values. Then I tested radix sort on a sample integer array and printed the sorted result.

While doing this homework, I practiced working with generic classes, linked structures, circular arrays, and sorting logic. The main thing I learned is that queues are useful not only as their own data structure, but also as part of solving other problems like radix sort.
