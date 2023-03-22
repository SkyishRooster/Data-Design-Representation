## JSON
1. JSON Example
- Simple JSON
```
{
  "firstName": "John",
  "lastName": "Smith",
  "isAlive": true,
  "age": 27,
  "homeNumber": "212 555-1234",
  "officeNumber": "646 555-4567",
  "mobileNumber": "123 456-7890"
}
```
- Convoluted JSON
```
{
  "firstName": "John",
  "lastName": "Smith",
  "isAlive": true,
  "age": 27,
  "address": {
    "streetAddress": "21 2nd Street",   # the output table may have columns like address.streetAddress, address.city, ...
    "city": "New York",                 # If another JSON file doesn't have "city" in "address", its correlated colmun would be blank
    "state": "NY",
    "postalCode": "10021-3100"
  }
}
```
- Arrays in JSON
Arrays:
  - An ordered collection of values
  - Encompasedd by "[]"
  - Separated by commas
```
{
  "firstName": "John",
  "lastName": "Smith",
  "isAlive": true,
  "age": 27,
  "phoneNumbers": [
  {
    "type": "home",
    "number": "212 555-1234"
  },
  {
    "type": "mobile",
    "number": "123 456-7890"
  }
  ]
}
```
2. JSON Attributes: 
-  **A method to structure information to be provided**
-  A lightweight text based data-interchange format
-  Completely language independent
-  Based on a subset of JavaScript
-  Easy to understand, manipulate, and generate
-  Supported by most backend techniques (Java, Python, etc.)
-  Can be natively parsed in JavaScript using eval()
-  Key-value pairs are separated by commas
-  Objects separated by curly squares "{}"
-  Flexibility in terms of input data type and data structure especially compared to SQL
- 

3. JSON Data Type
String
  - Wrapped in double quotes
  - Backslash escaped
Numeric
  - Integer
  - Real
  - Scientific
  - No octal or hex
  - No NaN or Infinity – Use null instead
Bool or Null
  - Booleans: true or false
  - Null: A value that specifies nothing or no value.


### Get the JSON file of a website - Transferring to API
eg. https://www.reddit.com/r/mildlyinteresting.json
  -> get the json file rather than the website https://www.reddit.com/r/mildlyinteresting/ itself
  
 
## APIs - Applicaiton Programming Interface

***Rule of thumb: If API is provided, use API rather than web scrapimg***

1. How to find APIs?
  - https://rapidapi.com
  - https://apilist.fun

2. UrbanDIctionary
  - https://api.urbandictionary.com/v0/define?term=bloghttps://api.urbandictionary.com/v0/define?term=blog
