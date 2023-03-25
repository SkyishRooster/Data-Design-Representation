1. to find all IP addresses (e.g., "46.60.226.75" should match)

FIND: [0-9]+\.[0-9]+\.[0-9]+\.[0-9]+



2. to find all E-Mail addresses (e.g., "a.ellis@bla.net" should match)

FIND: [a-z]\.[a-z]+@[a-z]+\.[a-z]+



3. to find all salaries

FIND: \b[0-9]{5,7}\b
OR
FIND: (?<=")[0-9]{5,7}(?=")



4. to transform the column "Last Seen" from US to year-month-day date format while leaving the rest as is. (e.g., "08/23/2012" should be changed to "2012-08-23" while leaving everything else as is)

FIND: ([0-9]{2})/([0-9]{2})/([0-9]{4})
REPLACE WITH: $3-$1-$2



5. to transform the column "SSN" from 9 digits to last four digits while leaving the rest as is. (e.g., "122725502" -> "5502")

FIND: ([0-9]{5})([0-9]{4})
REPLACE WITH: $2



6. to strip everything BUT the email column.

FIND: ^(.+)([a-z]\.[a-z]+@[a-z]+\.[a-z]+)(.+)$
REPLACE WITH: $2



7. to convert all rows to "Last Name" [TAB] "First Name" [TAB] "Last Seen" only (strip the rest). The "Last Seen" 
column should be in year-month-day format. ([TAB]s will allow you to copy and paste it's result into excel.)

FIND: ^(.+?),(.+?),(.+?)([0-9]{2})/([0-9]{2})/([0-9]{4})(.+)$
REPLACE WITH: $2\t$1\t$6-$4-$5



8. to strip everything BUT "Number of Children" and "Number of Logins" AND reorder its entries to be "Number of Logins" [TAB] "Number of Children".  ([TAB]s will allow you to copy and paste it's result into excel.)

FIND: ^(.+/.+?),("[0-9]"),(.+)("[0-9]{2}")
REPLACE WITH: $4\t$2


