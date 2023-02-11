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
2. JSON attributes: 
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

  
eg. https://www.reddit.com/r/mildlyinteresting.json
  -> get the json file rather than the website https://www.reddit.com/r/mildlyinteresting/ itself
  
 
