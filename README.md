![](MadLibs.JPG)    
Mad Libs
========
For this assignment we will use Python's `opne()` and `readline()` functions to read in a blank MadLib. Then we will use the `input()` function to ask the user for words from a particular part of speech (e.g. noun, adjective, verb, etc). Finally we'll use Python's `replace()` function to replace the blanks with user input. You may find the website [How to create a Mad Libs game in Python](https://www.teachwithict.com/mad_libs.html) and slides 168 - 179 of the [Computer Programming B slide presentation](https://docs.google.com/presentation/d/1rICcmNbnGYsB-cV_6EatPyzcOS2sId80Jh2kayUzm4Q/edit?usp=sharing) helpful.

Program requirements
------------------------------------------
1. Your Mad Libs program must use two files: A Python file with the program code and a seperate text file with a blank mad lib.
2. Your blank Mad Lib must be at least 5 lines long and have 3 or more parts of speech.
2. Your program will need a loop to go through the blank Mad Lib one line at a time replacing the blanks

Suggested steps to starting the assignment
------------------------------------------
1. For this assignment we will have two files:
    * a text (`.txt`) file with the blank Mad Lib
    * a Python file (`.py`) with the Python code that reads in the blank file and displays the modified version with user input
   
2. Let's start with the text file. Create a text file with your blank Mad Lib. You can use the following Old Macdonald lyrics, [AfraidOfTheDark.txt](AfraidOfTheDark.txt),  [SpookyStuff.txt](SpookyStuff.txt), [TalkLikeAPirate.txt](TalkLikeAPirate.txt) or make up your own.
```text
ADJECTIVE Macdonald had a NOUN, E-I-E-I-O
and on that NOUN he had an ANIMAL, E-I-E-I-O
with a NOISE NOISE here
and a NOISE NOISE there,
here a NOISE, there a NOISE,
everywhere a NOISE NOISE,
ADJECTIVE Macdonald had a NOUN, E-I-E-I-O.
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
['ADJECTIVE Macdonald had a NOUN, E-I-E-I-O\n', 'and on that NOUN he had an ANIMAL, E-I-E-I-O\n', 'with a NOISE NOISE here\n', 'and a NOISE NOISE there,\n', 'here a NOISE, there a NOISE,\n', 'everywhere a NOISE NOISE,\n', 'ADJECTIVE Macdonald had a NOUN, E-I-E-I-O.\n', '\n']
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
