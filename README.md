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
 * rST may represent a barrier for some experts who might otherwise be very
   interested in contributing tutorial material.

## Example tutorial

To demonstrate the auto-generation of web content from Jupyter notebook source
files, a tutorial already in Jupyter notebook form was needed. 
I grabbed [this CS231n tutorial][cs231] which is linked from [numpy.org][learn].

[cs231]: https://cs231n.github.io/python-numpy-tutorial/#numpy 
[learn]: https://numpy.org/learn/
