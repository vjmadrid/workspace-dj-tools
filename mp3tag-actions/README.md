# mp3tag-actions

This project represents a collection of operations ("actions") de [Mp3tag](https://www.mp3tag.de/en) defined to help prepare / clean up the music

This project stands out for:

* Provides a **collection of independent pre-build mp3tag actions** to prepare/clean up the music





## What is preparing / cleaning music?

It is the "personal" procedure that everyone has to organize their music collection and covers from getting the music, its edition at the information level (not contained), its classification and its storage within a persistence device (hard disk, portable hard disk, memory)

This procedure takes into account different aspects such as the name used in our music files, the directory structure we use, the tags we have and the way we use them

It is therefore essential that everyone finds their way of working, although several best practices have been found to be very helpful

Areas of best practices

* **Eliminate Duplicates** : unique values in those elements that require it -> remove repeated items
* **Parsing** : syntax analysis
* **Removing** : remove rare/normal characters, remove specific words, remove unnecessary spaces, ...
* **Conversion** : change type of an attribute
* **Data with noise** : errors in the information due to spelling mistakes, phonetics, word transpositions, typing errors, several values in a field, ...
* **Format** : compliance with specific rules in the data, add extra information, case conversion, ...
* **Standardization** : compliance with a representation scheme, 
* **Transformation** : replacing some words into others, replacing a specific character into another, ...
* **Structuring** : validate or generate a specific structure or scheme of the data, fild order, mandatory, optional, ...
* **Incomplete Data** : discover that specific attribute values are missing, add the missing information, set default values, ...
* **Inconsistency** : values that should not conflict with other values,  ...
* **Approximatioons** : readjustment of data
* ...





## What is an mp3tag action?

An [mp3tag action](https://help.mp3tag.de/options_format.html) is a feature of the program that makes it easy to apply pre-defined edits on the tags automatically 

Each one the defined actions :

* Should have a unique responsibility
* Should implement one of the operations considered in the areas of best practices
* Should apply to filenames and tags
* Should be user-defined
* Should have diferent types : Case conversion, convert codepage, Export, Format Value, ...

The actions are grouped into groups 

Each one the defined groups :

* Should be independent
* Should apply one single action
* Should allow for CRUD management
* Should be user-defined





## Important

* Before working with these actions or if you are going to try your own, it is ADVISED to create a backup folder, since the action or set of actions that you apply may leave your music INOPERATIVE

* Because everyone has their way of working, this collection may NOT serve you entirely because your needs are different, but it can serve as a guide or help you to plan your action

* There is a [forum](https://community.mp3tag.de/) in the tool itself that can be used to clarify your doubts





## Technological Stack

* [Mp3tag](https://www.mp3tag.de/en) - Audio file meta-information editor (Tag Editor)
* [Mp3tag Convert](https://help.mp3tag.de/main_converter.html) - Details about Convert
* [Mp3tag Action](https://help.mp3tag.de/options_format.html) - Details about Actions
* [Mp3tag Scripting Funcions](https://help.mp3tag.de/main_scripting.html)
* [Regular Expressions](https://en.wikipedia.org/wiki/Regular_expression) - Patterns for detecting expressions in texts

[Regular Expressions Online Validator](https://regex101.com/)

Note : Mp3tag provides 2 different syntaxes with different escape rules and logic





## Prerequisites

Define what elements are needed to install the software

* Latest version of the operating system
* Required Mp3Tag Version - **Mp3Tag 2.99 and higher**





## Installation App

Note :

* MP3TAG_HOME will be the name of the installation directory (mp3tag destination folder)
* MP3TAG_CONFIG will be the name of the application's configuration file (mp3tag settings folder)


### Steps to follow for WINDOWS

1. **Check** for other previous versions

    1.1. **Delete** the previous version

    ```bash
    C:\Program Files\Mp3tag
    ```

2. **[Download](https://www.mp3tag.de/en/download.html)** EXE app
3. **Execute** EXE file
4. **Follow** the instructions (select language, components choose MP3TAG_HOME directory, etc)
5. **Check** that it is installed on MP3TAG_HOME
6. **Check** Verify that you load the application


### Steps to follow for MAC
1. **Check** for other previous versions

    1.1. **Delete** the previous version

    ```bash
    /Users/ <user_name> /Library/Application Support/de.mp3tag.Mp3tag_*
    ```

2. **[Download](https://www.mp3tag.de/en/mac-osx.html)** app (Require Wine App)
3. **Unzip** the file
5. Allow applications from verified developers at System Settings > Security
6. Delete previous settings from 

6. Copy Mp3tag.app to your Applicantion folder


## Installation mp3tag-actions


### Steps to follow for WINDOWS

1. **Download** from the repository
2. Copy the actions in the MP3TAG_CONFIG folder for Actions

```bash
C:\Users\ <user_name> \AppData\Roaming\Mp3tag\Data\Actions
```

* If you use **Windows XP**

```bash
C:\Documents and Settings\ <user_name> \Application Data\Mp3tag\Data\Actions
```

- If you use **[portable](https://www.mp3tag.de/en/portable.html)** mode

```bash
%mp3tag% \Data\Actions 
```


### Steps to follow for MAC

1. **Download** from the repository
2. Copy the actions in the MP3TAG_CONFIG folder for Actions

    2.1. Finder > ⇧⌘G and then enter (~/Library/Application Support/)

```bash
/Users/ <user_name> /Library/Application Support/de.mp3tag.Mp3tag_<some_number>/drive_c/users/Mp3tag/data/sources
```

For example

```bash
/Users/vjmadrid/Library/Application Support/de.mp3tag.Mp3tag_15714760666332/drive_c/users/Mp3tag/data/
```






## Testing






## Use



That repository provides a pack of prebuild actions. You don't need to learn programming, just copypaste those actions into your program and user them on click.


## .mta Structure

Ejemplo de fichero de mte
```bash
[#0]
T=4
F=_ALL
1=\\b(?:(?:re)?mix(?:ed|ing)?|rmx)\\b
2=Remix
3=0
```

Detalle de la estructura del fichero

**T=<Action>**

T=1 'Case conversion'
T=2 'Replace'
T=3 Not listed in action types
T=4 'Regular expression'
T=5 'Format value'
T=6 'Remove duplicate fields'
T=7 'Guess values'
T=8 'Merge duplicate fields'
T=9 'Remove fields'
T=10 'Remove fields except'
T=11 'Convert codepage'
T=12 'Import cover from file'
T=13 'Export cover to file'
T=14 'Import text file'
T=15 'Export'
T=16 'Split field by seperator'

**F=<Field>**

xxx

**1=<Original String / regex>**

xxx

**2=<Replace original string with>**

xxx

**3=<Field>**

3=0 Means 'only as whole word' and 'case-sensitive comparison' not selected
3=1|0 Means 'only as whole word' selected and 'case-sensitive comparison' not selected
3=0|1 Means 'only as whole word' not selected and 'case-sensitive comparison' selected
3=1|1 Means 'only as whole word' selected and 'case-sensitive comparison' selected






## Versioning

**Note :** [SemVer](http://semver.org/) is used for the versioning.
To see the available versions access the repository tags





## Authors

* **Víctor Mad**