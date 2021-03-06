# Dictionary App Challenge

## Introduction

This was a coding challenge we did in Coder Academy's CCC course, where we had to create a small dictionary type app based on the lesson content that we had recently learned. For this project, I had the pleasure of working with [Gabriel Wong](https://github.com/GabrielWongAu). The programming features we were encouraged to use were:

* OOP paradigms
* The classmethod and staticmethod decorators
* Working with files
* Consuming APIs
* JSON manipulation
* Property decorators

## Features

Given we were under the time limit of 2 hours, there was a limit to the amount of features were we able to implement. However we managed to write an app which did the following: 

* User has the option to look up a word, when prompted the user will type in a word and if it exists in the API, returns the definition.
* If no word is present the error is handled gracefully.
* The user then has the option to add the word to their favourites. This is then stored in a file locally on the users machine.
* The user can view their favourite words at anytime from the app's main menu.

> For this app, we used the [Merriam-Webster](https://dictionaryapi.com/) API.

## Strategies

To implement the UI, we repurposed a module from the [String Section Rostering Utility](https://github.com/redbrickhut/StringSectionRosteringUtility) app, which allowed us to quickly render the view segment of the program. We encapsulated the data storage layer into its own class, and exposed its implementation through class methods. We also used a class to represent the word itself, encapsulating the API call to generate the word instances within as a static method.

## Unfinished Features

Whilst we weren't able to implement these features in the program itself, we laid the foundation for the following should there have been more time:
* The ability to select and remove words from favourites.
* The ability to see synonyms for a particular word. These synonym attributes would have been lazily instantiated.

## How to Install

If you're keen to check this out for yourself, you can do so by taking the following steps:
1. Make sure Python 3+ is installed on your machine. Download link [HERE](https://www.python.org/downloads/).

2. Make sure Pip is installed on your machine. This may be done by default when installing Python, however installation instructions can be found [HERE](https://pip.pypa.io/en/stable/installing/).
3. Clone or zip the repository to your local machine.
4. Navigate to the root folder of the project in your terminal and run:
```
pip3 install -r requirements.txt
```  
5. You will need to obtain your own API key from Merriam-Webster. Request a dictionary API key from [HERE](https://dictionaryapi.com/register/index). Upon doing so, create a new file called secrets.py in the src folder and add the following to it:
```
dictkey = "{your_api_key}"
```
6. Navigate to the src folder in the repository and run by executing: 
```
python3 main.py
```
