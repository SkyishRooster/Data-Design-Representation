### How does SQL index work?

*Without an index, data in a database usually gets stored as a heap, basically a pile of unordered, unsorted rows*

**Binary search**: for ordered stored column (eg.id), "where id = 105" command does binary search -> <br>
    Compare the id you select with "105", if the id selected is smaller, then search within the the first half; otherwise, search within the other half
    
Primary key – which in MySQL can be identical to an index – is something like an auto-incrementing integer <- stored in order <br>

**Creating indexes** <- a way of *letting your table be sorted by multiple columns*, which lets you get binary search efficiency on multiple filter columns.


*hashCode function (Java) / hash method (Python)* - convert strings into integers (space out the strings in the whole space of interger)
    - eg. "David": 65805908
    - eg. "Zavid": 86123370

**Why not index everything**: 
1. Creating indexes takes up extra storage (hidden columns with the index numbers would be created and stored)
2. Indexes affect the insertion speed:<br>
    *Database is living: there is always data comes in (insert) and data comes out (query)*
    -> if we index everything, even one single entry would need a lot much time to complete the insertion
    
    
## MongoDB
### Attributes
1. MongoDB = "Humongous DB"
2. NoSQL - Document-based
3. Open-source
5. "High performance, High availability"
6. Auto-scaling


