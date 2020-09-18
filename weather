import requests, json
# base URL
BASE_URL = "https://api.openweathermap.org/data/2.5/weather?"
API_KEY = "81f8689c8e41121db123f43120eebf5c"

# upadting the URL
def take(city): 
  URL = BASE_URL + "q=" + city + "&appid=" + API_KEY
  # HTTP request
  response = requests.get(URL)
  # status code of the request
  if response.status_code == 200:
     # data in the json format
    data = response.json()
    # main 
    main = data['main']
    # Region
    country = data['sys']['country']
    # getting temperature
    temperature = main['temp'] - 273.151
    # lon
    lon = data ['coord']['lon']
    # lat
    lat = data ['coord']['lat']
    # timezone
    timezon = data ['timezone'] 

  

  
    print(f"{city:-^30}")
    print(f"Country: {country}")
    print(f"Temperature:" +  str("%.2f" % (temperature)))
    print(f"longitude: {lon}")
    print(f"latitude: {lat}")
    print(f"UTC_time:"  'UTC+' +  str("%.2f" % (timezon/3600)) if timezon/3600>0 else 'UTC_time:UTC' + str("%.2f" %(timezon/3600)))

  else:
    # showing the error message
    print("Error in the HTTP request")
  return 

take('Saint Petersburg')
print ('\n')

take('Chicago')
print ('\n')

take('Dhaka')
print ('\n')
