cookie is unique for anyone
your cookie is different when you visit different web, but you have the same cookies when you visit the same page
browser / website use cookies to identify the visitor

every page only have one id

Select class "col-md-6" (not unique)
  inside of the class, select the first "p"
  
  
### CASE: TigerDirector
https://www.tigerdirect.com/applications/SearchTools/item-details.asp?EdpNo=1163565&CatId=4935&csid=_86

*Monitor on the price of the laptop*
1. go to the "Elements" panel
2. use the mouse icon on the top left corner
3. hover on the price
4. locate at the class "sr-only" which stands for '$449 and 99 cents'


### Cookies
The content of delivered by the website varies if the request information (accept-language, user-agent, browser) is different.
 - You may mimic the user agent for variant use
 - How to stay log in: cookies (key-value pairs: eg. MUID, SUID) <- where the website sit down
      - Cookies -> geolocation, resolution of the screen, operating system, update status, ...
      - However, cookies are needed for stay logged in on a website <- Deactivate third-party cookies
            eg. when visit NY Times, Google/FB won't be able to get your cookies 

### Selector
- div.cdf <- classes
- div#dfg <- ID
- div:contains('text')
- div:has('text')
- div:not('text')
- a['href'] <- attribute
- body p <- ancestor child

*Some website change / randomize the class name. -> Look for tags that remain the same for a longer preriod. eg. h1, h2, ...*
Counting headers is better than counting divs

Close a window to prevent cookies retaining


### CASE: Shanghai Air Pollution
https://aqicn.org/city/shanghai

*Goal: Retrieve hourly air pollution parameters*
1. Select whatever you are interested in; 
      eg. div.aqiwidget-table-x
2. Create an infinite loop for requesting the website automatically;
3. IMPORTANT: Put pause time (in seconds);
4. Save the output into a csv file

