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
1. install chrome driver
2. import selenium
3. using selenium is an easy way to communicate with the browser (remote controlling a browser)
4. However, you need to debug much more (update the version of chrome driver, changes in the website design, ...)


***set up the driver***
```
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.common.by import By

driver = webdriver.Chrome(executable_path='"C:\ChromeDownloads\chromedriver_win32\chromedriver.exe"')
driver.implicitly_wait(10)
driver.set_script_timeout(120)
driver.set_page_load_timeout(10)

# Specify the website address
driver.get("https://google.com")
```

***remotely control the browser***
```
inp = driver.find_element(By.CSS_SELECTOR, "input[type=text]")
# search for "Selenium" on Google remotely
inp.send_keys("Selenium\n")
```

***always close the driver if you previously created one***
```
time.sleep(10)          #close the browser after 10 seconds automatically
driver.quit()
```

