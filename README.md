SANJEEV

0%

1. Compiling the C++ I trust
2. Re-deriving the gradient by hand
3. Counting problems (still not the point)
4. Breaking one small thing on purpose
5. Putting it back together

Tap anywhere to skip

# Hi, I’m Sanjeev.

I’m a CS student at NIT Srinagar (class of 2028), and I learn best when something is actually broken.

I don’t trust a model until I’ve seen the math. So here is the smallest version of one: a ball rolling down a loss curve.

Learning rate 0.12 Click or tap the curve to drop a point.

try the right side, then crank the learning rate up

## What I’m like

Give me a slow query, a weird bug or a half-working schema and I’ll happily lose a weekend to it. The projects where the answer is sitting in a tutorial three tabs over don’t teach me much.

Right now I’m pulled toward machine learning and data science, but I’m doing it the slow way: the probability, the linear algebra and the statistics most tutorials skip. It takes longer. It’s also the only way I end up believing the number at the end.

If something in one of my repos is useful, take it and run. If it’s broken, even better. Tell me why.

## Things I’m building

### GitHub bug scanner

Watches pushes and pull requests, looks for bugs, posts what it finds to GitHub and a dashboard, then tracks whether they get fixed.

still on paper

### Dining Philosophers

The classic OS synchronisation problem, written in C++17 for my operating systems coursework.

coursework, but it’s a good bug magnet

The rest lives on [GitHub](https://github.com/sanjeev-kumar-patel).

## How I read a problem

I’m past 400 problems on LeetCode and GeeksforGeeks, mostly in C++. The count was never the point. What I track is how quickly I can look at something new and see its shape: graphs, DP, greedy, binary search, and always the complexity.

```
// Smallest speed that still finishes in time.
// The question I ask first: is the answer monotonic?
int lo = 1, hi = *max_element(a.begin(), a.end());
while (lo < hi) {
    int mid = lo + (hi - lo) / 2;
    if (canFinish(a, mid, h)) hi = mid;
    else lo = mid + 1;
}
return lo;
```

if yes, binary search the answer

[My LeetCode profile](https://leetcode.com/u/sanjeev-kumar-patel/)

## What I reach for

For problem solving

C++ first, C when I want to be closer to the machine.

For the web

JavaScript, React, Node.js, Express, HTML and CSS, with MySQL or MongoDB behind it.

Day to day

Git and GitHub, Linux and Bash, VS Code, Postman.

Still learning

Python, NumPy, pandas, scikit-learn and Jupyter, properly, not just the API.

## The roadmap, mistakes included

1. **DSA and C++**Graphs and DP. I’m not rushing past this; everything else sits on top of it.
2. **Math and statistics**Probability and linear algebra, the parts tutorials skip.
3. **ML fundamentals**Build from scratch first, then reach for the library.
4. **Data science**Real datasets and honest results.

## Say hello

I’m up for talking about DSA, backend design, debugging stories, or how to learn ML without just calling `.fit()`. If you found a bug in one of my repos, I especially want to hear from you.

[Write an email](mailto:sanjeev2005p.05@gmail.com) [LinkedIn](https://www.linkedin.com/in/sanjeev-kumar-patel/) [GitHub](https://github.com/sanjeev-kumar-patel)

Built by hand, on graph paper. Stars on a repo are noticed.
