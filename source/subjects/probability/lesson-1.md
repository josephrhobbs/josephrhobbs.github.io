# Lesson 1: What Are the Chances?

~

When was the last time you used a probability to describe an event?  We all use probability so frequently that you _probably_ can't even remember.  For example, you might have wondered if it would rain tomorrow, so you checked the weather forecast.  But the forecast won't give you a straight answer, because meteorologists have no idea whether it will rain tomorrow or not!  Instead, it told you there was a certain _probability_ of rain tomorrow.  But what does it mean if there's a 25 percent chance of rain tomorrow?

We all understand probability intuitively, but when we go to express what it actually _is_, we start to struggle.  We often describe probability as "X percent of the time".  This makes sense when describing a repeatable experiment, such as a coin toss.  If you toss a coin 100 times, it will probably land heads about 50 times, so "50 percent of the time it lands heads" (or "in 50 percent of experiments it lands heads") is an accurate description.  But the sentence "25 percent of the time it will rain tomorrow" is utter nonsense... it's either going to rain, or it's not.  More importantly, tomorrow will only happen once, and "tomorrow" is not a repeatable experiment in the same way that a coin toss is.

As we embark on this journey through the theory of probability, it's important to remember that probability _per se_ doesn't have a rigorous mathematical definition.  Instead, we'll talk about probability in terms of its properties.  Let's begin by defining some important terminology that we'll be making extensive use of shortly.

## Outcomes and the Sample Space

Whenever we use probability, we always begin by defining clearly our _sample space_.  The sample space is a set containing all possible _outcomes_.  An outcome \( \omega \) is a measurable, quantifiable result from an experiment or observation.  The sample space \( \Omega \) is a set containing every possible outcome \( \omega \).  It's very important that in the sample space, outcomes are _mutually exclusive_ of one another and _collectively exhaustive_ of the sample space.  In other words, the outcomes must be defined in such a way that _one_ and _exactly one_ outcome always occurs.  For example, in a weather forecast, the following sample space is valid.

\[ \Omega = \{ \text{rain}, \text{no rain} \} \]

This is a valid sample space, because the outcomes "rain" and "no rain" are mutually exclusive (they can't both happen) and collectively exhaustive (one outcome must happen).  In contrast, the following sample space is not valid.  Can you see why?

\[ \Omega = \{ \text{rain}, \text{cloudy} \} \]

This is not a valid sample space because it might rain _and_ be cloudy (not mutually exclusive) or it might not rain and not be cloudy (not collectively exhaustive).  Note that sample spaces can be infinitely large, as long as the two conditions are satisfied.  For example, imagine that you ask your friend to think of an integer.  The sample space here is

\[ \Omega = \mathbb{Z} = \{ \cdots, -3, -2, -1, 0, 1, 2, 3, \cdots \} . \]

This sample space is infinitely large, but it's still a valid sample space.  All outcomes are mutually exclusive (you asked your friend to think of only one number) and collectively exhaustive (the sample space contains every possible integer).

## Probability

Probability is defined as a _function_, denoted \( \mathbb{P}(\cdot) \), mapping subsets of \( \Omega \) to positive real numbers.  Here, and throughout our journey, we'll use the dot symbol \( \cdot \) as a simple placeholder for another symbol.  Mathematically, we write

\[ \mathbb{P} : \mathcal{P}(\Omega) \rightarrow \mathbb{R} . \]

The notation \( \mathcal{P}(\cdot) \) indicates the _power set_ operation.  The power set of a set \( \Omega \) is the set containing _all possible subsets_ of \( \Omega \).  In a simple example, consider our previous sample space.

\[ \Omega = \{ \text{rain}, \text{no rain} \} \]

The power set of \( \Omega \) contains every possible subset of \( \Omega \).

\[ \begin{align*} \mathcal{P}(\Omega) = \{ \{  \}, \{ \text{no rain} \}, \{ \text{no rain} \}, \{ \text{rain}, \text{no rain} \} \} \end{align*} \]

Note that \( \mathcal{P}(\Omega) \) includes the null set \( \emptyset = \{ \} \) because this too is a subset of \( \Omega \) (and every other set, except the null set).  As discussed previously, there's no rigorous definition of what probability _means_... it is simply defined as a function mapping elements of \( \mathcal{P} \) to real numbers in \( \mathbb{R} \).