# An example site for creating web-based NumPy tutorials from Jupyter Notebooks

This is a minimal example of how one could set up a repository for generating
tutorials from user-submitted Jupyter notebooks.
Note that this is only *one possible* such configuration, and is only 
intended for demonstration/discussion purposes.

## Motivation

The purpose here is to investigate the feasibility of a tutorial-generation
mechanism based on Jupyter notebooks:

 * Jupyter notebooks are a common format for communicating scientific
   information.
 * rST may present a barrier for some people who might otherwise be very
   interested in contributing tutorial material.

## Example tutorial

To demonstrate the auto-generation of web content from Jupyter notebook source
files, a tutorial already in Jupyter notebook form was needed. 
I grabbed [this CS231n tutorial][cs231] which is linked from [numpy.org][learn].

[cs231]: https://cs231n.github.io/python-numpy-tutorial/#numpy 
[learn]: https://numpy.org/learn/

## Generating the "site"

Sphinx is configured with the appropriate extensions to execute the notebooks
and generated webpages from them. To accomplish this from a fresh repo:

1. Install the dependencies:
   
   ```
   pip install -r requirements.txt
   ```

   To execute the notebooks, you'll also need to install the dependencies for
   the tutorial(s) themselves:

   ```
   pip install -r content/requirements.txt
   ```

2. Build and view

   ```
   make html && <your_browser> _build/html/index.html
   ```

## Adding your own tutorials

If you have your own tutorial in the form of a Jupyter notebook and you'd like
to try it out on the site:

1. Add your notebook to the `content/` directory
2. Update `content/requirements.txt` with the dependencies for your tutorial
3. Update the `toctree` in `index.rst` to include your new entry
