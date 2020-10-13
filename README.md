# test
Automated tests/python

from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.common.keys import Keys
import time
import os
import unittest

#class Loginweb(unittest.TestCase):

#open browser
	#def openbrowser(self):
		driver = webdriver.Chrome()
	#	driver = self.driver
		driver.get("https://www.shopback.com.tw/")
		time.sleep(1)

#Find login/signup button
	#def test_login(self):
		loginpath = '//div[@id="header"]/div/header/div[1]/div[1]/div[1]/div[3]/div/span/div'
		login_click = driver.find_element_by_xpath(loginpath).click()
		time.sleep(1)

#Login
		loginbutton = '//*[@id="auth-popup-container"]/div/div[2]/div[2]/div/div/div[2]/div[1]/div/div[2]'
		login_click = driver.find_element_by_xpath(loginbutton).click()
		time.sleep(1)

#login with email
		login_email = '//*[@id="auth-popup-container"]/div/div[2]/div[2]/div/div/div[2]/div[1]/div/div/div/div[1]'
		login_click = driver.find_element_by_xpath(login_email).click()
		time.sleep(1)

#Input email
		login_input = '//*[@id="auth-popup-container"]/div/div[2]/div[2]/div/div/div[2]/div[1]/div/div[1]/input'
		email_input = driver.find_element_by_xpath(login_input)
		email_input.send_keys("test123@test123.com")
		time.sleep(1)
		next_button = '//*[@id="auth-popup-container"]/div/div[2]/div[2]/div/div/div[2]/div[1]/div/button'
		next_click = driver.find_element_by_xpath(next_button).click()
		time.sleep(1)

#Input password
		login_pw = '//*[@id="auth-popup-container"]/div/div[2]/div[2]/div/div/div[2]/div[1]/div/div[1]/input'
		pw_input = driver.find_element_by_xpath(login_pw)
		pw_input.send_keys("sbtest555")
		time.sleep(1)
		next_button = '//*[@id="auth-popup-container"]/div/div[2]/div[2]/div/div/div[2]/div[1]/div/button'
		next_click = driver.find_element_by_xpath(next_button).click()
		time.sleep(1)


#class searchkeyword(unittest.TestCase):

#search keyword
#	def test_search_keyword(self):
		search_path = '//*[@id="header"]/div/header/div[1]/div[1]/div[1]/div[2]/div[1]/input'
		search_bar = driver.find_element_by_xpath(search_path)
		time.sleep(1)
		search_bar.send_keys("cetaphil")
		time.sleep(1)
		search_bar.send_keys(Keys.ENTER)


#select product
	#def test_select_product(self):
		product_path = '//*[@id="__next"]/div/div/div/div/div[2]/div/div[2]/div[1]/div/div[2]/div/div/div/div/div'
		product = driver.find_element_by_xpath(product_path).click()
		time.sleep(1)

#select store
	#def test_select_store(self):
		newtab_xpath = driver.find_element_by_xpath('//*[@id="__next"]/div/div/div/div/div[2]/div/div[2]/div[1]/div/div[2]/div/div/div/div/div/a').get_attribute("href")
		driver.execute_script("window.open();")
		driver.switch_to_window(driver.window_handles[1])
		driver.get(newtab_xpath)
		time.sleep(1)

		store_path = '//*[@id="#offers"]/div/table/tbody/tr[1]/td[1]'
		store = driver.find_element_by_xpath(store_path).click()
		time.sleep(1)

#buy
	#def test_buy(self):
		buy_path = '/html/body/div[4]/div/div/div[3]/button'
		buy = driver.find_element_by_xpath(buy_path).click()
		time.sleep(1)



#if __name__ == "__main__":
#	unittest.main()



