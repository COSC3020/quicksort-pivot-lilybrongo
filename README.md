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

Knowing these possibilities, within all good values, each element has a 50% (1/2) chance of being within the middle of the data. so $(1/2)^3 = 1/8$. Since there are six possible arrays where two values are good, three that contain one less than and three that contain one more than. These six possibilities would be $(1/2)^2 * (1/4) * 3 = 3/16. So for both the less than and more than cases it would be $2 * 3/16 = 3/18$. For the extreme cases the probablity of only one good value would be $(1/2) * (1/4)^2 * 6 = 3/16). In the end the total probablity would be the sum of these possibilities, $1/8 + 3/8 + 3/16 = 11/16$ which would be approximately 68.75%. Since the first element selection has a probablity of 50% that the pivot will fall in the middle. Whereas the median-of-three has an overall probability of 68.75%. In the end the median-of-three method increases the probability of selecting a good pivot.

I used the lectures and videos from class to get the initial probabilities adn get a starting point. Referrenced geeksforgeeks: https://www.geeksforgeeks.org/median-of-an-unsorted-array-in-liner-time-on/  for a further explination. Talked with students Daniel Collins and Will Greiner about how to handle this problem and the probabilities.

I certify that I have listed all sources used to complete this exercise, including the use
of any Large Language Models. All of the work is my own, except where stated
otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is
suspected, charges may be filed against me without prior notice.



