from selenium import webdriver
import unittest
import HtmlTestRunner
#import time
from selenium.webdriver.common.keys import Keys

class GoogleSearch(unittest.TestCase):

    @classmethod
    def setUpClass(cls):
        cls.driver = webdriver.Chrome(executable_path='../drivers/chromedriver.exe')
        cls.driver.implicitly_wait(10)
        cls.driver.maximize_window()

    def test_search_automationstepbystep(self):
        self.driver.get("https://google.com")
        self.driver.find_element(by = "name",value="q").send_keys("Continous Integration Tools")
        self.driver.find_element(by= "name",value="btnK").send_keys(Keys.ENTER)

    def test_search_raghav(self):
        self.driver.get("https://google.com")
        self.driver.find_element(by = "name",value="q").send_keys("Jenkins")
        self.driver.find_element(by= "name",value="btnK").send_keys(Keys.ENTER)

    @classmethod
    def tearDownClass(cls):
        cls.driver.close()
        cls.driver.quit()
        print("Test Completed")

if __name__ == '__main__':
    unittest.main(testRunner=HtmlTestRunner.HTMLTestRunner(output='C:/Users/vdmtn/PycharmProjects/pythonProject2/pythonProject/Selenium/reports'))
