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


### Get vs. Post
**GET request:**
*In a url:*
- Everthing before "?" denotes the page address (like file paths on local computer)
      eg. https://google.com/search?q-who+am+i    <- "search" is not a solid option, other representation exists like "s"
      eg. https://amazon.com/s?k=stupid+gifts     <- variable "k" relates to search for items <= enables searching for same/different specified items every often
- "&" connects variable kay-value pairs after "?" (page)

**POST request:**
*Developer Tool:*
- post username and password: the information can be found through
- Network -> session -> Payload
      eg. https://flightaware.com/account/session


### How to stay logged in?
**Everything goes around with cookies**
- It's the server that set cookies to our browser
*In the html file of the website:*
- login -> the informatin is stored in element "form" (action, method, name, ...)
- "input" -> deliver key-value pairs ("name", "value") such as "referer", "mode", "username", "password", "token", "submit", ...
        - input type: 
            - "hidden" <- invisible elements;
            - "text" <- visiable text;
            - "password" <- concealed text;


*Every website support javascripts:*
Usecase examples:
1. Amazon shopping cart update without the whole page reload
2. Facebook more feeds loading without the whole page reload
- Javascripts send tiny updates to the server, empowering dynamic page loading
