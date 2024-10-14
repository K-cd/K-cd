매크로 사전 준비

pip install selenium
https://sites.google.com/a/chromium.org/chromedriver/downloads 크롬 드라이버 설치 경로

from selenium import webdriver
from selenium.webdriver.chrome.options import Options
from selenium.webdriver.common.by import By
import time

options = webdriver.ChromeOptions()
driver = webdriver.Chrome()

#data = 

driver.get('https://www.zerohongdae.com/reservation')
time.sleep(1)


reserve_date = driver.find_element(By.XPATH, '//*[@id="calendar"]/div/div/div/div/div[2]/div[20]')
reserve_theme = driver.find_element(By.XPATH, '//*[@id="themeChoice"]/label[1]')
reserve_time = driver.find_element(By.XPATH, '//*[@id="themeTimeWrap"]/label[2]')
reserve_btn1 = driver.find_element(By.XPATH, '//*[@id="nextBtn"]')

reserve_date.click()
time.sleep(2)
reserve_theme.click()
time.sleep(2)
reserve_time.click()
time.sleep(2)
reserve_btn1.click()
time.sleep(5)

#임시 코드
