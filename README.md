ListRank-MF
===========

A Java implementation of ListRank-MF as mentioned in:
Y.Shi, M.Larson, and A.Hanjalic. List-wise Learning to Rank with Matrix Factorization  for Collaborative Filtering. ACM RecSys 2010.

ListRank-MF combines a list-wise learning-to-rank algorithm with  matrix factorization (MF) to produce a ranking list of items.

## Example
The program takes in input in the form (user, item, rating) pairs, seprated by a single tab.  A valid input example is:
```
U01 I23 5.0
U01 I53 5.0
U01 I14 5.0
U01 I66 5.0
U5  I14 5.0
U77 I66 5.0
```
Where we have user U01 have rated item I23 a 5.0

We can run the following
```
ListRankMF lrmf = new ListRankMF(r);
System.out.println("User: U01 \t Item:I23: "+ lrmf.finalPrediction("U01","I23"));
``` 
to get a predicted score of item I23 for user U01. To get a ranked list for a user, we run the finalPrediction method for each item in the dataset for that user. Sorting the list in descending order in terms of the score gives us the ranked list. 

## Note
The code hasn't been tested thoughrly. If you find any mistakes, please do let me know.
If you use this code in any projects/research, I would like to learn more about how you used it.

## License 
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

