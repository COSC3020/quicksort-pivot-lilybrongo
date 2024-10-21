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

It is known that there is a 1/2 chance of choosing a good pivot value (Lecture 01 Sorting- slide 34). If we use the median-of-three method, the reason that there is a half chance of choosing a good pivot value is because there is a chance that the pivot will be less than or greater than that good pivot solection. The median-of-three pivot method chooses the first, middle, and last elements in the array, and out of these three it will return the median value. In order for it to be considered a good pivot, it has to create two partitions, one being at most a size of 3n/4 (Lecture 01 Sorting- slide 34). With this chosen method, there will be a 1/2 chance of being a good pivot. 

Percentage calculations:

Less than good pivot = L
Good pivot = G
More than good pivot = M

With the Median-of-Three method, the possible arrays are:

(LLL), (LLG), (LLM), (LGG), (LGM), (LGL), (LML), (LMM), (LMG)

(GGG), (GGL), (GGM), (GLM), (GML), (GLL), (GMM), (GMG), (GLG)

(MMM), (MML), (MMG), (MLL), (MGG), (MLG), (MGL), (MLM), (MGM)


