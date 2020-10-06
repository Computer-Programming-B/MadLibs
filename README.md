![](MadLibs.JPG)    
Mad Libs
========
For this assignment we will use Python's `readline()` function to read in a blank MadLib. Then we will use `input()` function to ask the user for words from a particular part of speech (e.g. noun, adjective, verb, etc). Finally we'll use Python's `replace()` function to replace the blanks with user input.

Suggested steps to starting the assignment
------------------------------------------
1. For this assignment we will have two files:
    * a text (`.txt`) file with the blank Mad Lib
    * a Python file (`.py`) with the Python code that reads in the blank file and displays the modified version with user input
   
2. Let's start with the text file. Create a text file with your blank Mad Lib. You can use the following or make up your own:
```text
Adjective Macdonald had a Noun, E-I-E-I-O
and on that Noun he had an Animal, E-I-E-I-O
with a Noise Noise here
and a Noise Noise there,
here a Noise, there a Noise,
everywhere a Noise Noise,
Adjective Macdonald had a Noun, E-I-E-I-O.
```
3. Give the file a meaningful name like `MadLibs.txt`
4. Now we'll start writing the Python program
5. Add the following code to your Python program (the `.py` file) that opens the text file and assigns it to a variable:
```Python
f = open('MadLibs.txt','r')
madlibText = f.readlines()
print(madlibText)
```
6. Run the program. You should see output like:
```
['Adjective Macdonald had a Noun, E-I-E-I-O\n', 'and on that Noun he had an Animal, E-I-E-I-O\n', 'with a Noise Noise here\n', 'and a Noise Noise there,\n', 'here a Noise, there a Noise,\n', 'everywhere a Noise Noise,\n', 'Adjective Macdonald had a Noun, E-I-E-I-O.\n', '\n']
```
7. `madlibText` is a list. Each item in the list is a line from the text file.
8. Now we need to add code to get user input for each part of speech. In the example text there are:
   * Adjective
   * Noun
   * Animal
   * Noise
9. Here's some sample code we could use for user input:
```Python
noun = input("Enter a noun: ")
print("Rumble in the " + noun)
```
10. Now we'll use Python's `replace()` function to replace the blank `Noun` in the first line of `madlibText`. Change the `print` to
```Python
line = madlibText[0].replace("Noun",noun)
print(line)
```
11. Now create a loop to go through each line in `madlibText` and change every occurance of the blank `Noun`
12. Finally, add more user input for the other parts of speach and replace those as well

*This assignment is based on an assignment at [Te@ch with ICT](https://www.teachwithict.com/mad_libs.html)*
