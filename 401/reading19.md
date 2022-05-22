# Automation and you

## [Reg Ex](https://docs.python.org/3/library/re.html)

`variable = re.compile(pattern)` - Takes a regex that you would like to save to use many times through the program.

`pattern.search(string[, pos[, endpos]])` Scan through string lookng for first expression match

`pattern.match(string[, pos[, endpos]])` Return a matching object or return none if it doesn't match. 

`pattern.fullmatch(string[, pos[, endpos]])` Attempts to match full string

`pattern.split(string, maxsplit=0)` Identical to split() but using the pattern.

`pattern.findall(string[, pos[, endpos]])` similar findall() but using the pattern provided. 

`pattern.pattern`  Shows the saved pattern 

## [Shutil](https://pymotw.com/3/shutil/)

High level file operations

Shutil has several operations which support copying, removal, packing and unpacking of objects/files. 
