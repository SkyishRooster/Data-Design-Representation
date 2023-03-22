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
