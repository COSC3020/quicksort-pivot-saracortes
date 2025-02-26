# Quicksort Pivots

in the lectures I only briefly mentioned strategies for determining a good pivot
for quicksort. The implementation on the slides simply picks the leftmost
element in the part of the array that we consider as a pivot. I also mentioned a
few other ways of picking a good pivot, e.g. randomly.

Median-of-three is also a good way of picking a pivot -- inspect the first,
middle, and last elements of the part of the array under consideration and
choose the median value. Using the probabilities for picking a pivot in a
particular part of the array (in the same way as we did on slide 34), argue
whether this method is more or less (or equally) likely to pick a good pivot
compared to simply choosing the first element. Assume that all permutations are
equally likely, i.e. the input array is ordered randomly.

Your answer must derive probabilities for choosing a good pivot and
quantitatively reason with them.

Add your answer to this markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.


Picking a good pivot in quicksort will help split the array in a more even way and it also keeps the sorting fast. If we pick the first element as the pivot, its probability of being a good pivot depends on its random placement in the array. Because all permutations of the array are equally likely, any element could be at any index. This is why, the probability that the first element falls within the middle third (between the 33rd to 66th percentile) is approximately 33.3%. The median-of-three (choosing the middle value from the first, middle, and last elements) is a better choice because it is about 5/9, which is a 56% chance of picking a good pivot. Since 56% > 33%, the median-of-three is more likely to keep quicksort efficient and will also prevent slow cases.
