# my_project
from selenium.webdriver import Firefox
from selenium.webdriver.firefox.options import Options
import urllib
import requests

#Определяем браузер
browser = Firefox() 
#Ссылка на сайт
browser.get('https://netpeak.ua/') 
#Поиск ключеового слова (скрытой ссылки) на страницу и переход по клику.
link = browser.find_element_by_partial_link_text('Карьера').click() 
#Поиск ключеового слова (скрытой ссылки) на страницу и переход по клику
link = browser.find_element_by_partial_link_text('Я хочу работать в Netpeak').click() 
#Поиск фрагмента страницы по его id и внесение значений (ключей).
search_form = browser.find_element_by_id('inputName').send_keys(' Vlas lv') 
search_form = browser.find_element_by_id('inputLastname').send_keys(' Bon dy') 
#Поиск фрагмента страницы по его имени (name) и внесение значений (ключей).
search_form = browser.find_element_by_name('by').send_keys('1999') 
search_form = browser.find_element_by_name('bm').send_keys('июля') 
search_form = browser.find_element_by_name('bd').send_keys('8') 
search_form = browser.find_element_by_id('inputEmail').send_keys('vladyslav.bondyk@barakooda.com') 
search_form = browser.find_element_by_id('inputPhone').send_keys('+38000000000') 
search_form = browser.find_element_by_name('up_file').send_keys('D:\photo_uno.jpg') 
#клик по кнопке "отправить резюме"
browser.find_element_by_id('submit').click() 
#Переход на первую страницу. Не разобрался как отобразить в скрипте переход на главную страницу сайта через ссылку логотип.
browser.get('https://netpeak.ua/') 
