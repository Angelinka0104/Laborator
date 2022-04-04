# Laborator
Лабораторная работа 1
from bs4 import BeautifulSoup
import requests
import lxml.html as html
import pandas as pd
#import re
#from re import sub
#from decimal import Decimal
#import io
#from datetime import datetime
# поиск в определённой зоне
url = 'https://en.wikipedia.org/wiki/Six_degrees_of_separation'#переменная url
response = requests.get(url)#переменная url передается функции requests.get Результат присваивается переменной response
soup = BeautifulSoup(response.text, 'lxml')# переменная текста ответа
quotes = soup.find_all('span', class_='text')#переменной quotes будет присвоен список элементов span с классом text из HTML-документа.
for quote in quotes:
    print(quote.text)
#print(soup)
#Переменная soup содержит полный HTML-код страницы с результатами поиска.
