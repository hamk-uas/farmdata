<!-- Translation sync: this file is up to date with the Finnish source 2026/Luennot.md as of commit 80080b5696ee64becb99e488730d36c80ea93424. To catch up, translate the changes shown by: git diff 80080b5696ee64becb99e488730d36c80ea93424 HEAD -- 2026/Luennot.md (then update the commit hash here). -->
Autumn 2026

© 2026 HAMK Hämeen Ammattikorkeakoulu. Authors: Pirita Rantala, Olli Koskela, Olli Niemitalo

# 1. Lecture 28.10.2026
<!-- Do not change the lecture heading, because Moodle deep-links to it! Add a short description below! -->

This lecture covers Colab, the use of AI, and Python basics part 1.

### Python

Python is a programming language that is very popular for data analysis. Writing a program for data analysis is convenient because a program only needs to be written once and can then be used repeatedly with different input data. The capabilities of Python can be extended using *modules*, for example in order to easily manipulate tabular data or for plotting, etc. Modules typically have their own online documentation that can be consulted.

Because of Python's popularity, AI tools are very familiar with it and you should seek help using AI (AI) chats. Over the past year, a more modern way of utilizing AI, using AI agents that independently develop programs, has become more powerful than chats. Agents are able to create source code files, run them, test program functionality, and fix bugs. Agent features may also be available in AI chats.

To help AI assist you to the best of its ability, you should tell it in your "prompt" what problem you are trying to solve, what thoughts you have about the solution, how confident you are about them, or whether you want AI to choose the solution methods itself. If an error occurs during program execution, the error message itself is useful information for AI to understand the error, and you should provide it.

Artificial intelligence (AI) tools can help you and you can use those freely in this course for code generation. For you it is probably more important to "get the job done" than to become a fluent Python programmer. You can think of AI as an assistant that writes code for you. Google Gemini AI is covered in the next section. Other useful AI tools for Python code generation include ChatGPT, Gemini, Copilot, Mistral, Grok, Deepseek, Manus, and Claude. Using them to a small extent is free and increasingly many of them are able to run and test code themselves. When credits run out in one service you can switch to another.

If you intend to send AI information that is confidential or private, make sure you have permission to do so. You may need to check the AI service's terms of use and privacy policy for how the data you send is used. Also consider whether you trust the service provider.

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

Colab gives access to Gemini artificial intelligence (AI) features such as *Generate code* button for creating code based on a prompt entered, and the *Explain error* button.

### Switching Google account

The profile icon in the top right corner opens a menu where you can use the Add account option to sign in with a new account.

<img src="assets/datatalous/media/image6.png" style="width:7.31771in;height:2.87876in" />

## Python basics part 1

This subsection covers the basics of Python programming, using code examples. Type or copy-paste each code example into a code cell in Colab, and run the cell. Try to understand the result. Modify the code as instructed and run it again. You can also create a new cell and write your own code in it.

In Python, you can create your own variables. A variable always refers to some value. Values have different types. We will become familiar with some of these types in this section. Depending on the type of value the variable refers to, the variable or rather its value can be used in different ways.

The Python interpreter runs a Python program or code cell line by line from top to bottom. If the interpreter encounters an error, execution is halted and an error message is displayed. The Python interpreter remembers the values of all variables from previously executed code. You can delete all created variables by clicking *Runtime*→*Restart*. This will not delete local files saved during execution.

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

In Python, spaces at the beginning of each line are used to divide code into blocks, which will be explored later. Otherwise, spaces can be freely added between code to make the code more readable. Appropriate use of spaces makes code more readable.

The last line is also an example of calling a function, in this case Python's built-in print function. A function is called by writing comma-separated input values to parentheses after the function name. A function may return a value. There are many built-in functions, and you can also write your own functions.

### Exercise pause during the lecture

**Change the input numbers and see how the result changes.**

**Create versions of the code that perform 1) subtraction and 2) multiplication.** See: [<u>Python operators</u>](https://www.w3schools.com/python/python_operators.asp).

**Calculate the square root of a number.** You can google or ask AI how to do it.

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

[Weekly exercise 1](Exercise1.md)

# 2. Lecture 4.11.2026
<!-- Do not change the lecture heading, because Moodle deep-links to it! Add a short description below! -->

[Weekly exercise 2](Exercise2.md)

# 3. Lecture 11.11.2026
<!-- Do not change the lecture heading, because Moodle deep-links to it! Add a short description below! -->

[Weekly exercise 3](Exercise3.md)

# 4. Lecture 18.11.2026
<!-- Do not change the lecture heading, because Moodle deep-links to it! Add a short description below! -->

[Weekly exercise 4](Exercise4.md)

# 5. Lecture 25.11.2026
<!-- Do not change the lecture heading, because Moodle deep-links to it! Add a short description below! -->

[Weekly exercise 5](Exercise5.md)

# 6. Lecture 2.12.2026
<!-- Do not change the lecture heading, because Moodle deep-links to it! Add a short description below! -->

[Weekly exercise 6](Exercise6.md)

# 7. Lecture 9.12.2026
<!-- Do not change the lecture heading, because Moodle deep-links to it! Add a short description below! -->

(No new weekly exercise)

# After the lecture series

The report presentations session is on 15.12.2026. Try to utilize the programmatic data analysis skills you've gained in your presentation and report. For example, you can acquire and merge external data into your project data and analyze them together, using Python in whatever work stages you want.

The exam will include questions about the weekly exercises.
