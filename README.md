# How-to-Talk-Generative-Approach-to-Classification

December 23, 2020

I appreciate comments. Shoot me an email at noel_s_cruz@yahoo.com!

Hire me! 😊

- So today we will introduce a simple and powerful approach
to building classifiers.
It's called the generative approach
and it's based on probability distributions.
So the main idea with the generative approach
is to fit each class separately
with a probability distribution.
Okay?
So for example, here we have a training set
of about 15-20 points and what we do
is that we first look only at one label,
so here there are two labels, pluses and minuses.
So we start by looking just at the pluses
and we fit a model to them.
And then we look only at the minuses,
and we fit a model to those.
So maybe we get something like this.
So on the left, we have an ellipse shape distribution
that we fit to the pluses
and then we have another ellipse shaped distribution
that we fit into the minuses.
That's a total learning process.
Now, when a new point comes along,
say, a point like this, and we want to classify it,
we just ask ourselves
Was this new point more likely to have come
from the red distribution or the blue distribution?
Under which of these two distributions
does it have higher probability?
And that's it.
Okay, so that's a high level overview
of the generative approach.
So let's, let's be a little bit more concrete
and put down some details.
Okay, so here's a picture in which
there are three classes, or three labels.
Let's call them one, two, and three.
So the label space y is just the set one, two, and three.
And let's say that the data is very simple.
The data just has one feature,
so the data points are one-dimensional
and they can just be plotted on the line.
So in order to fit a generative model,
what we do, is we take our training set
and first we look only at the points whose label is one,
and we fit a probability distribution to them.
So maybe, for example, we get this distribution over here,
the red one, okay?
Let's call that one P1(x).
The distribution for label one.
Then, we take the training set again,
and look only at the points whose label is two,
and we fit a probability distribution to those.
Maybe that looks like P2(x) over here.
And finally we look at the remaining points,
the ones that have labeled three,
and we get a probability distribution to that.
So that's P3(x).
And now we have these three separate
probability distributions.
We need a little bit more information, as well.
Let's say, for instance, that label one
makes up 10% of the training set.
So out of the training points,
one tenth of them have label one.
So what we'll do is say Pi(1) equals 10% or .1.
Let's say label two makes up 50% of the training set.
So we'll say Pi(2) equals 50% or .5
and the remaining 40% of the training set
comes from label three.
So, we say Pi(3) equals .4.
Now, at the end of this, what we have is
the following pieces of information.
For each class, j, so j is one, two, or three,
we have the probability of that class,
which is just a number, like .1, .5, or .4,
and we also have the distribution of data in that class,
which is what we have been calling P sub j,
P set 1, P set 2, P set 3.
And these pieces are built information are enough
to fully specify the joint distribution between x and y.
So the probability of any pair, x y,
is the probability of that label, y,
times the probability of seeing data x under that label y.
So the probability of x given y.
Now the probability of seeing label y
is simply Pi sub y
and the probability of seeing point x
under the distribution of label y, is P sub y of x.
So we have the full probability distribution
over x and y.
So now a new point x comes along and we want to classify it.
We want to determine a label, y, for it.
Which label do we pick?
Well, the mostly likely label,
the one that maximizes the probability of x and y.
Concretely, what we would do in this case,
with three classes, is that we take our point x
and we calculate Pi one times P1(x) and that's some number.
We calculate Pi two times P2(x)
and we calculate Pi three times P3(x).
And we take whichever of these is the largest.
If the last one is the largest, for example,
we say the label equals three.
Okay, so that's it for a high-level overview
of the generative approach to classification.
Some of the details might seem a little mysterious
at this point because they rest
on various probabilistic concepts.
So what we'll do next is to do a little bit of a review,
a little bit of a tour, of the relevant probability
and then we'll come back and we'll flesh out
this approach and see it in action.
Thank you.

I included some posts for reference.

https://github.com/noey2020/How-to-Talk-of-Fitting-a-Distribution-to-Data-

https://github.com/noey2020/How-to-Talk-of-Host-of-Prediction-Problems

https://github.com/noey2020/How-to-Talk-of-Useful-Distance-Functions

https://github.com/noey2020/How-to-Talk-of-Improving-Nearest-Neighbor

https://github.com/noey2020/How-to-Talk-of-Prediction-Problems

https://github.com/noey2020/How-to-Talk-Matlab-Tricks-and-Tweaks

https://github.com/noey2020/How-to-Talk-Trading-and-Investing

https://github.com/noey2020/How-to-Work-in-Matlab-Development-Environment

https://github.com/noey2020/How-to-Talk-Vaccines

https://github.com/noey2020/How-to-Talk-Regression-in-Matlab

https://github.com/noey2020/How-to-Get-Started-in-Matlab

https://github.com/noey2020/How-to-Convert-Data-from-Web-Service-Using-Matlab

https://github.com/noey2020/Quote-for-the-Day

https://github.com/noey2020/How-to-Talk-Good-Investment-Strategy

https://github.com/noey2020/How-to-Talk-of-Good-Plan

https://github.com/noey2020/Thought-for-the-Day

https://github.com/noey2020/How-to-Talk-Stock-Watch-of-the-Day

https://github.com/noey2020/How-to-Talk-Data-Science

https://github.com/noey2020/How-to-Talk-Fundamental-Analysis

https://github.com/noey2020/How-to-Read-Company-Profiles

https://github.com/noey2020/How-to-Import-Data-from-Spreadsheets-and-Text-Files-Matlab-Without-Coding

https://github.com/noey2020/How-to-Talk-Model-of-Stock-Market-Prices-

https://github.com/noey2020/How-to-Talk-Digital-Wallets

https://github.com/noey2020/How-to-Talk-Investing

https://github.com/noey2020/How-to-Double-Your-Money-in-5years

https://github.com/noey2020/How-to-Talk-Matlab

I appreciate comments. Shoot me an email at noel_s_cruz@yahoo.com!
