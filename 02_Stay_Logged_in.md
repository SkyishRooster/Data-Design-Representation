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
- The first thing: open the developer tool and click "log in"
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


User --login--> Server (submit all login information and no data else)
Server --cookies--> User (store the cookies in the browser)
      *Cookies are generated on the server side*
*from now on*
User --cookies + login--> Server (to Login)


Sometimes one request is enough (login info); more times requests 2 requests (login info + cookies)


Two-stage request is required when random generalized login info is also required when logging in
      So the first stage needs to get the random info and the cookies
      And the second stage posts to login
      

## Selenium

