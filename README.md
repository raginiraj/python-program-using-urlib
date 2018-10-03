# python-program-using-urlib
#python program to check value of indian currency
import urllib.request
import time
def value_of_indian_rs():
      source_page=urllib.request.urlopen("https://tradingeconomics.com/india/currency")
      data=source_page.read().decode("utf 8")
      checkpoint=data.find("new record")+18
      end=checkpoint+7
      new_value=float(data[checkpoint:end])
      return(new_value)
while(1):
    print(value_of_indian_rs())
    time.sleep(28800)

