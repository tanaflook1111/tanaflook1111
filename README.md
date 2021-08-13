import time
from selenium import webdriver
from selenium.webdriver.chrome.options import Options
from selenium.webdriver.common.action_chains import ActionChains
options = Options()
options.add_argument("--window-size=500,1080")
driver = webdriver.Chrome(options=options)
driver.get("https://dash.imageedits.com/ie_login?Block=Login")

Email=driver.find_element_by_css_selector("input[type='email']")
Email.send_keys("Thanadolpoolyiam@gmail.com")

password=driver.find_element_by_css_selector("input[type='password']")
password.send_keys("ASpirine1011")

time.sleep(3)

driver.find_element_by_xpath("//button[@class='bubble-element Button clickable-element'][@tabindex='3']").click()

#Take Order Page
driver.get("https://dash.imageedits.com/dashboard_editor?uuidnav=1614396793054x615853962006759600&uuiduserdets=1617624512287x747914310516736000&uuidbus=&uuidorder=&uuidproject=&uuiddelivery=&busoveruser=")

time.sleep(3)

#List work
driver.find_element_by_xpath("//div[@class='bubble-element Group clickable-element'][@tabindex='8']").click()

time.sleep(3)

#Assign
driver.find_element_by_xpath("//button[@class='bubble-element Button clickable-element'][@tabindex='11']").click()
