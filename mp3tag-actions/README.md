# mp3tag-actions

This project represents a collection of operations ("actions") of [Mp3tag](https://www.mp3tag.de/en) defined to help prepare / clean up the music-

This project stands out for:

* Provides a **collection of independent pre-build mp3tag actions** to prepare/clean up the music
* Provides a **collection of independent pre-build action groups** based on the scope





## What is preparing / cleaning music?

> "Each way of classifying a thing is only one way of handling it for a certain particular purpose." William James

It is the **"personal" procedure** that many people apply to **organize/classify** their **music collection** according to **your needs**, allowing :

* *To have a better order/classification when storing in a persistence device (hard disk, portable hard disk, memory, etc.)*
* *To be much more efficient when we look for it inside the persistence device or from the use of some specialized application*
* *To have useful and much more complete information when using it*

The **edition** will be applied at the level of **information** and **meta-information** of an mp3 file after obtaining it and just before saving it. Although it can be edited at any time, it should be taken into account whether it may have any consequences.

Since **"there are as many ways of doing things as there are ways of drinking water"** it is essential that everyone finds the way they are most comfortable and the way that allows them to be more productive, no matter how rare or complex it may be.

This procedure can vary significantly from person to person, so many of the **problems** that occur are **frequent** and **repeated** to everyone. Some **best practices** can be applied to solve these problems,


### Areas of best practices

There are some specific areas of application where action can be taken. Some areas can be :

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

An [mp3tag action](https://help.mp3tag.de/options_format.html) is a feature of the program that makes it easy to apply pre-defined edits on the tags automatically.

As the concept of action can encompass different meanings, I found it interesting to establish a classification according to the complexity that an action may have to help understand this concept.

ADD IMAGE


### Action

Minimum work unit and responsible for performing a single task

Features :

* *Should have a single responsibility -> perform a clearly defined task*
* *Should have a identifiable name*
* *Should implement one of the operations considered in the area of best practices*
* *Should apply to filenames and tags*
* *Should be user-defined*
* *Should have diferent types : Case conversion, convert codepage, Export, Format Value, ...*
* *It can be independent or defined within a group*


### Action Group

Set composed of one or more actions which corresponds to the first grouping level

It is provided by the application

Features :

* *Should have a single scope of application (general or specific)*
* *Should have a identifiable name*
* *Should be independent*
* *Should be user-defined*


### Procedure

Set composed of one or more groups corresponding to extra grouping levels

Features :

* *Should have a higher level of scope (general or specific)*
* *Should have a identifiable name*
* *Should be independent*
* *Should be user-defined*




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


Note : Mp3tag provides 2 different syntaxes with different escape rules and logic


### Useful resources

[Regular Expressions Online Validator](https://regex101.com/)
[Regular Expressions Online Visualizer](https://jex.im/regulex/)

To work with the formats used, a conversion from "to" is required

* "\\\\" is required by the mp3tag expression
* "\\" is required by any of the validators






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

N/A






## Use

That repository provides a pack of prebuild actions. You don't need to learn programming, just copypaste those actions into your program and user them on click.





## Versioning

**Note :** [SemVer](http://semver.org/) is used for the versioning.
To see the available versions access the repository tags





## Authors

* **Víctor Mad**