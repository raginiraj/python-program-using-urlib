# python-program-using-urllib
#python program to check value of indian currency
import urllib.request
import time
def value_of_indian_rs():
      source_page=urllib.request.urlopen("https://tradingeconomics.com/india/currency")
      data=source_page.read().decode("utf 8")
      checkpoint=data.find("The")
      end=checkpoint+53
      new_value=float(data[checkpoint:end])
      return(new_value)
while(1):
    print(value_of_indian_rs())
    time.sleep(28800)

