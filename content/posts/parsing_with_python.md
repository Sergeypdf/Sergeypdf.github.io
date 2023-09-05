title: Parsing in Python
date: 2022-06-10
description: Pyparsing module for beginners
tag: python
project: Python Course for Beginners
platform: Python Workshop
link: http://example.com

Parsing, or syntactic analysis, is the process of matching a sequence of words or symbols to a formal grammar. For example, for a piece of code:

	import matplotlib.pyplot  as plt


The following grammar is in place: it starts with the keyword "import," followed by the name of the module or a chain of module names separated by dots. After that comes the keyword "as," and then our chosen name for the imported module.

As a result of parsing, for example, it may be necessary to arrive at the following expression:

	{ 'import': [ 'matplotlib', 'pyplot' ], 'as': 'plt' }


This expression represents a Python dictionary that has two keys: 'import' and 'as'. The value for the 'import' key is a list that sequentially lists the names of the imported modules.

For parsing, regular expressions are commonly used. Python has a module called 're' (regular expression) for this purpose. If you haven't worked with regular expressions before, their appearance can be intimidating. For example, for the code string 'import matplotlib.pyplot as plt,' it might look like:

	r'^[ \t]*import +\D+\.\D+ +as \D+'
