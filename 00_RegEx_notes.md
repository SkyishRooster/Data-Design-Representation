## All Upper & Lower Letters
[A-Za-z]
it is different from [A-z] because there are characters fall between Z and a in ASCII

## Sequence of Number
[0-9]+

## A sequence of numbers of certain digits (eg. 4)
[0-9]{'number of digits'}
  eg. [0-9]{4}

### A four-digit sequence that was note followed by a digit
[0-9]{4}(?![0-9])

## () making a named group / object
### Names for capturing groups are sequent numbers by default
  eg. Transform Date Format: 07/16 2022 -> 2022-07-16
    FIND: ([0-9]{2})/([0-9]{2}) ([0-9]{4})
    REPLACE: $3-$1-$2

## ? for non-greeedy expressions
  eg. Extract email address
  FIND: .+?([^,]+@[^,]+).+
  REPLACE: $1
  
## Put metacharacters at the very beginning of a expression is equivalent to using  '\'
  eg. ([-0-9]) = ([0-9\-])
  
## 
