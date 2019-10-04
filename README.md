# Score-distribution

Programming exercise #1: Score distribution
Suppose we wish to re-score the points of interest (POIs) in our database so that their scores fit a particular distribution.  The goals of this process:

1.	All POIs should end up with a score between 0 and 10.
2.	There should be significantly more POIs with score between k-1 and k than between k and k+1 for all k in [1..9].
3.	Very few POIs should end up with a score between 9 and 10.  Such high scores should really only go to the very best POIs in the world: aim to have about 0.1%-0.2% of POIs in this range.
4.	The algorithm should work regardless of the range and distribution of the input scores.

Note that we have lots of POIs in our database about which we know very little.  For such POIs we have no indication that they're any good (so we score them low) or that they're any better/worse than other POIs that we don't know much about (so they should end up scoring similarly).  Hence the bottom-heavy distribution.

Write a (preferably python) script to read POI scores from a file, assign them new scores according to the above criteria and write them to another file.  You are welcome to use libraries like scipy and pandas if you like.  One target distribution that could be used would be a Zipfian distribution, but feel free to surprise us with your choice.

We have provided three sample data files containing POI IDs and their corresponding scores:

http://data2.triposo.com/exercises/exercise1/raw_scores.list1.gz
http://data2.triposo.com/exercises/exercise1/raw_scores.list2.gz
http://data2.triposo.com/exercises/exercise1/raw_scores.list3.gz

For the first, your script must preserve the relative order of the POI scores.  For the second, it should do something sensible (ideally letting us know what and why).  The third one is an artificial dataset, included simply to help you test that your script is not dependent on the distribution of the input scores.

Time is limited in life and in work, and nobody can do everything they'd like to, so we don't expect perfect solutions that meet all the criteria.  Do what you can in a reasonable amount of time and document any outstanding issues and (in brief) any thoughts you might have about how to solve them.

