## Method chaining
To view the tutorial notebook, click [here](https://nbviewer.jupyter.org/github/joosthvanderlinden/pandas-method-chaining-tutorial/blob/master/group%20tutorial%20on%20method%20chaining.ipynb).

It is common practice and encouraged in the Pandas documentation to use 'method chaining' or function 'pipes.' I use method chaining, for example, to read in my data and to group/sample/slice before plotting. The advantages of method chaining include:
- It saves you from having to define a lot of intermediate variables.
- You can clean your data directly after you read it in, combining all your pre-processing steps into a single command.
- You can plot your data directly after grouping/sampling/slicing/etc.
- It looks good. Your code will read like a story; top to bottom, left to right.

Or, in Tom Augspurger's words:

> "My scripts will typically start off with large-ish chain at the start getting things into a manageable state. It's good to have the bulk of your munging done with right away so you can start to do Science™"

Source and fantastic walkthrough: http://tomaugspurger.github.io/method-chaining.html (read all 7 parts)

Other tips:
- Use pandas build-in methods when possible, like `resample()` in the tutorial. Otherwise, define your own function and use `pipe()`.
- As always, prefer vectorized operations over iterative operations (see `correct_flow_rate_fast()` in the tutorial)
- Familiarize yourself with the difference between `.loc`, `.iloc` and pandas assignment in general ([link](http://tomaugspurger.github.io/modern-1.html))

Resources:
- http://pandas.pydata.org/pandas-docs/stable/generated/pandas.read_csv.html
- http://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.pipe.html
- http://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.resample.html
