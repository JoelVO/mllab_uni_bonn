[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=7636704&assignment_repo_type=AssignmentRepo)
# Exercise 1

You can install jupyter-notebooks and the necessary python packages either using Anaconda 
(https://www.anaconda.com/products/individual) or on a Linux-based operating system in the following way using virtual environments:

1. Make sure you are using python3, which is the default since python2 is not supported any more.
2. Install virtualenv (if not already installed) via 
	"sudo -H pip install virtualenv"
3. Go to the directory of your choice and create a virtual environment via
	"virtualenv .mllab"
4. Once created you should activate the environment by running
	"source .mllab/bin/activate"
5. Then, to install the necessary packages for python use the
   requirements.txt file and then run
	"pip install -r requirements.txt"
6. Finally, you can run and edit your jupyter-notebooks via
	"jupyter-notebook NameOfYourNotebook.ipynb"

You can learn some more about python and numpy using the provided two notebooks 
- Introduction to Python.ipynb
- Introduction to NumPy.ipynb

When you have worked on the tasks from sheet 1, stage and push your work to your repository. Create a pull request with the changes you made.
