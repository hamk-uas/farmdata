Autumn 2026

© 2026 HAMK Hämeen Ammattikorkeakoulu. Authors: Olli Koskela, Olli Niemitalo

# 1. Lecture 28.10.2026 Colab, Python basics part 1

## Python

Python is programming language that is very popular for data analysis. Writing a program for data analysis is convenient because a program only needs to be written once and can then be used repeatedly with different input data. Because of Python’s popularity, there is plenty of english-language help available on Internet, available through for example Google searches and AI chats. The capabilities of Python can be extended using *modules*, for example in order to easily manipulate arrays of numbers, or for plotting, etc. Modules typically have their own on-line documentation that can be consulted.

You don’t need to memorize how exactly something can be done in Python. Just google or ask AI about it! Typically, many people have had the same problem that you might have, and have asked for help for example in [<u>Stack Overflow</u>](https://stackoverflow.com/), a free question and answer service. Sometimes it is enough to use the error message as a search key or AI prompt.

Artificial intelligence (AI) tools can help you and you can use those freely in this course for code generation. For you it is probably more important to “get the job done” than to become a fluent Python programmer. You can think of AI as an assistant that writes code for you. Google Colab built-in Gemini AI is covered in the next section. Other useful AI for Python code generation include ChatGPT, Gemini, Copilot, Grok, Manus, and Claude. They are free for small-scale use and are increasingly able to run and test code.

## Colab

Colab is a Google service that is available to HAMK students through their Google accounts. In Colab, Python can be used interactively in a Jupyter Notebook.

While not covered in this course, it is possible to install Python and Jupyter Notebook on your own computer. Visual Studio Code is a popular code editor, and Git is a very popular tool for software version control. Version controlling means storing a cumulative history of your source code during development. GitHub is a very popular service to host version controlled software projects.

**Create a new notebook** by opening [<u>https://colab.research.google.com/</u>](https://colab.research.google.com/). You can enter a notebook name of your choice.

**Locate your notebook in Google Drive** by clicking *File*→*Locate in Drive*. You may wish to move the notebook to a folder.

When running Python code in Colab, the code is run in a *runtime*, which is a Google-hosted virtual machine. A runtime is automatically created for you the first time you run a code cell in the notebook.

**Run an empty code cell** by pressing the play button. After a moment, this will have created a runtime for you.

The runtime is a virtual machine, and it has its own local files. All of the runtime’s local files will be deleted when the runtime is deleted. This sometimes happens unexpectedly, and also happens if there is for a period of time no connection from your computer, for example if the notebook browser tab is closed, if your computer goes to sleep, or if your Internet connection goes down. Any data stored in Python variables is also lost upon deletion of the runtime. However, the notebook containing your code is stored in Google Drive and will not be deleted. Unlike with Google Docs documents, you may need to manually save changes you made to the notebook, although sometimes changes get saved automatically.

**Examine the runtime** by exploring the *Runtime* menu.

**Examine the local files on the runtime**, by clicking the folder icon on the left.

**Try creating new text and code cells.**

**Edit the contents of the new cells.**

**Run code in a cell** by pressing Ctrl-Enter (Windows) or Cmd-Enter (Apple) or the play button of the cell.

Colab gives access to Gemini artificial intelligence (AI) features such as being able to *generate* code given a natural language prompt, and the *Explain error* button. A very convenient way to use Gemini in Colab is to write a comment in the code and let Gemini write the code below the comment. For this to work, you may need to create a runtime (a normal thing to do when using Colab, see below).

### Changing the used Google account

Profile icon in the right top corner opens a menu where Add account (Lisää tili) option allows to add HAMK Google account if it isn’t already in the list.

<img src="assets/analyzing-data/media/image5.png" style="width:7.31771in;height:2.87876in" />

## Python basics part 1

This subsection covers the basics of Python programming, using code examples. Type or copy-paste each code example into a code cell in Colab, and run the cell. Try to understand the result. Modify the code as instructed and run it again.

In Python, you can create your own variables that refer to a value. There are different types of values. We will become familiar with some of those in this section. Depending on what type of value the variable refers to, you have access to different way of using the variable.

A python program or a code cell is run line-by line from top to bottom by the Python interpreter. If the interpreter encounters an error, the execution will be interrupted and an error message will be shown. The python interpreter remembers the values of any variables from previously run code. To forget all variables, click *Runtime*→*Restart session*. This will not delete local files stored in the runtime.

### Comments, variables, types (numbers, strings), basic math, print

```python
# This is a comment. Comments begin with # and will not be run.

# Assign numerical values to variables
x = 5
y = 2.5

# Assign the result of a basic calculation to a variable
result = x + y

# Print the value of a numerical variable
print(result) # Prints 7.5
```

Spaces can be freely added to the code between words to make the code more readable, except at the beginning of each line where they are used to split the code into blocks (to be explained later) in Python.

The last code line above is an example of calling a function. A function is called by writing comma-separated input values to parentheses after the function name. Functions may return a value. There are many built-in functions and you can also write your own functions.

### Exercise pause during the lecture

**Change the input numbers and see how the result changes.**

**Change the calculation to 1) subtraction and 2) multiplication.** See: [<u>Python operators</u>](https://www.w3schools.com/python/python_operators.asp).

**Calculate the square root of a number.** Hint: You can Google how to do it, or ask AI.

### Lecture continues

```python
# Assign a string value to a variable
sentence = "My name is"

# Concatenate strings
name = "Peter"
sentence = sentence + " " + name

# Print the value of a string variable
print(sentence)

# Do the same using a formatted string
sentence = f"My name is {name}"
print(sentence)
```

### Exercise pause during the lecture

**Add a second name using another variable.**

**Use the second name in the sentence.** Hint: For example resulting in “Our names are Peter and Eva”.

[Exercise 1: Fibonacci numbers](Exercise1.md)

# 2. Lecture 4.11.2026

[Exercise 2](Exercise2.md)

# 3. Lecture 11.11.2026

[Exercise 3](Exercise3.md)

# 4. Lecture 18.11.2026

[Exercise 4](Exercise4.md)

# 5. Lecture 25.11.2026

[Exercise 5](Exercise5.md)

# 6. Lecture 2.12.2026

[Exercise 6](Exercise6.md)

# 7. Lecture 9.12.2026

[Exercise 7](Exercise7.md)

# 8. Report presentations 15.12.2026
