# Mp3tag Action Templates




## Structure ".mta" file

Example of a mta file : 

```bash
[#0]
! Replaces errors in the value with the text Acapella =
T=4
F=_ALL
1=(A|a)\\s?capp?ell?a
2=Acapella
3=0
```

### Detail of the file structure

[#XXX] : Identifier and order indicator 
T : Action Type
F : Target of the action


### Action Type Values

T=1  : 'Case conversion'
T=2  : 'Replace'
T=3  : Not listed in action types
T=4  : 'Regular expression'
T=5  : 'Format value'
T=6  : 'Remove duplicate fields'
T=7  : 'Guess values'
T=8  : 'Merge duplicate fields'
T=9  : 'Remove fields'
T=10 : 'Remove fields except'
T=11 : 'Convert codepage'
T=12 : 'Import cover from file'
T=13 : 'Export cover to file'
T=14 : 'Import text file'
T=15 : 'Export'
T=16 : 'Split field by seperator'



## File Template by Type



### T=1 'Case conversion'

[https://help.mp3tag.de/options_format.html#case](https://help.mp3tag.de/options_format.html#case)

```bash
[#XXX] : Identifier and order indicator
T=1 : 'Case conversion' Type
F= : Target (_ALL, _DIRECTORY, _FILENAME, _FIELDNAME, _TAGS AND FIELDS)
1= : Case convertion (lower case (4), Mixed Case (1), Sentence (8), Upper Case (2))
2= : Word begin from/any of "xxx" or nothing
```


### T=2 'Replace'

[https://help.mp3tag.de/options_format.html#replace](https://help.mp3tag.de/options_format.html#replace)

```bash
[#XXX] : Identifier and order indicator
T=2 : 'Replace' Type
F= : Target (_ALL, _DIRECTORY, _FILENAME, _TAGS AND FIELDS)
1= : Original value
2= : Replace value
3=VALUE_1|VALUE_2 : Configuration
```

Configuration -> VALUE_1|VALUE_2

* VALUE_1 : "Only as whole word" boolean value (1 true / 0 false)
* VALUE_2 : "Case-sensitive comparison" boolean value (1 true / 0 false)


### T=3 Not listed in action types

xxx

```bash
[#XXX] : Identifier and order indicator 

```


### T=4 'Replace with regular expression'

[https://help.mp3tag.de/options_format.html#regexp](https://help.mp3tag.de/options_format.html#regexp)

```bash
[#XXX] : Identifier and order indicator 
T=4 : 'Replace with regular expression' Type
F= : Target (_ALL, _DIRECTORY, _FILENAME, _TAGS AND FIELDS)
1= : Regular Expression value
2= : Replace matches with value
3= : "Case-sensitive comparison" boolean value
```

3=0 Means 'only as whole word' and 'case-sensitive comparison' not selected
3=1|0 Means 'only as whole word' selected and 'case-sensitive comparison' not selected
3=0|1 Means 'only as whole word' not selected and 'case-sensitive comparison' selected
3=1|1 Means 'only as whole word' selected and 'case-sensitive comparison' selected


### T=5 'Format value'

[https://help.mp3tag.de/options_format.html#format](https://help.mp3tag.de/options_format.html#format)

```bash
[#XXX] : Identifier and order indicator 
T=5 : 'Format value' Type
1= : Format String (For example : %artist% - %title%)
F= : Target (_DIRECTORY, _FILENAME)
```


### T=6 'Remove duplicate fields'

[https://help.mp3tag.de/options_format.html#removedupes](https://help.mp3tag.de/options_format.html#removedupes)

```bash
[#XXX] : Identifier and order indicator 
T=6 : 'Remove duplicate fields' Type
```

No parameters used


### T=7 'Guess values'

[https://help.mp3tag.de/options_format.html#guess](https://help.mp3tag.de/options_format.html#guess)

```bash
[#XXX] : Identifier and order indicator 

```


### T=8 'Merge duplicate fields'

[xxx](xxx)

```bash
[#XXX] : Identifier and order indicator 

```


### T=9 'Remove fields'

[xxx](xxx)

```bash
[#XXX] : Identifier and order indicator 

```


### T=10 'Remove fields except'

[https://help.mp3tag.de/options_format.html#removeex](https://help.mp3tag.de/options_format.html#removeex)

```bash
[#XXX] : Identifier and order indicator 
T=10
F= : FIELDs
```


### T=11 'Convert codepage'

[xxx](xxx)

```bash
[#XXX] : Identifier and order indicator 

```


### T=12 'Import cover from file'

[xxx](xxx)

```bash
[#XXX] : Identifier and order indicator 

```


### T=13 'Export cover to file'

[xxx](xxx)

```bash
[#XXX] : Identifier and order indicator 

```


### T=14 'Import text file'

[xxx](xxx)

```bash
[#XXX] : Identifier and order indicator 

```


### T=15 'Export'

[xxx](xxx)

```bash
[#XXX] : Identifier and order indicator 

```


### T=16 'Split field by seperator'

[xxx](xxx)

```bash
[#XXX] : Identifier and order indicator 

```
