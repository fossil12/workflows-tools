# Python for Machine Learning

_This is meant for people familiar with some programming, but never did any Python and/or ML (Machine Learning) before._

## Install Python

I use [hombrew](https://brew.sh). So getting the most recent [Python](https://www.python.org) (3) is one line:

```bash
brew install python3
```

I install all modules with `pip3`. (There are other package managers but so fare I couldn't see their advantage.)

As fare as I know there are no reasons left to start learning Python 2.7 now. If you don't trust me, listen to [this podcast episode](https://talkpython.fm/episodes/show/100/python-past-present-and-future-with-guido-van-rossum) with the inventor of Python, Guido van Rossum.

## Learn Python

It's always hard to find a good introduction tutorial to a new language if you already have some experience with programming. For Python I'm really happy with the [official one](https://docs.python.org/3/tutorial/index.html). It strikes the right balance between introducing the language and relating to familiar concepts from other languages.

As it is quite long and takes some time to get through I recomment to do the first nine chapters and leave the rest out if you are in a hurry.

## Interactive Notebooks

For "prototyping" Python code a really nice tool exists ([IPython](http://ipython.org)) which is used by [Jupyter Notebooks](https://jupyter.org). If you have Python installed it's one command to install it.

```shell
pip3 install jupyter
```

Then you navigate in the terminal to the folder where you want to create and/or open a notebook and run:

```shell
jupyter notebook
```

Look at the keyboard shortcuts (hit `H` in a notebook) as they are really helpful for faster prototyping.

Side note: These notebooks really [remind](https://twitter.com/fossil12/status/844228444225454080) me of the [Swift Playgrounds](https://developer.apple.com/swift/playgrounds/) (Yes, they are even older).

## Editor for Python

As I'm not a big fan of IDEs not native to the OS (like [PyCharm](https://www.jetbrains.com/pycharm/) written in Java) I use [Sublime Text 3](http://www.sublimetext.com) to write Python scripts. To run the scripts using the Python installed with homebrew I created a new "Build System" file `Python-3.sublime-build` in the Packages folder.

```json
{
    "cmd": ["/usr/local/bin/python3", "-u", "$file"],
    "file_regex": "^[ ]*File \"(...*?)\", line ([0-9]*)",
    "selector": "source.python"
}
```

Now you can run your open script in ST with `cmd+B` (Tools > Build).

## ML in Python

This is a list of tutorials I looks into so for that capture various aspects of ML modules for Python.

- [Numpy Primer](https://github.com/dalab/lecture_cil_public/blob/master/exercises/ex1/npprimer.ipynb) (A longer tutorial can be found [here](https://docs.scipy.org/doc/numpy-dev/user/quickstart.html). Not tried by myself.)
- [Titanic Data Science Solutions](https://www.kaggle.com/startupsci/titanic/titanic-data-science-solutions) (Tutorial for Kaggle's intro competition)
- [Linear Regression Example](http://scikit-learn.org/stable/auto_examples/linear_model/plot_ols.html)
- [Matplotlib: Beginner's Guide](http://matplotlib.org/index.html) (Not tested so far, but it looks really good.)

Using those I found these useful libraries so far

- [Numpy](http://www.numpy.org) for fast numerical calculations
- [Pandas](http://pandas.pydata.org) for easy importing and shaping of (training/testing) data
- [scikit-learn](http://scikit-learn.org) for many ML algorithms
- [Matplotlib](http://matplotlib.org/index.html) for plotting

Want to install all of them? Here you go:

```shell
pip3 install numpy
pip3 install pandas
pip3 install scipy 	# Needed for scikit-learn
pip3 install scikit-learn
pip3 install matplotlib
```

## Basic Python Script Skeleton

```python
#!/usr/bin/env python3

# Import modules
import x

# Main function
def main():
    pass

if __name__ == '__main__':
    # This code is only executed if this is started as the main script
    main()
```

***

Written by [David Keller](https://davidkeller.me). License: [Attribution-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/)