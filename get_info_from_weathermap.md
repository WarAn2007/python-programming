# getter the info from current city in live time
```py
import requests
def converter_of_temperature(K_temp):
    Celsius = K_temp - 273.15
    return Celsius

main_url = 'https://api.openweathermap.org/data/2.5/weather?'
API_KEY = open('API_key.txt', 'r').read()

city = "Samarkand"

url = f"{main_url}appid={API_KEY}{city}"

response = requests.get(url).json()

K_temp = response['main']['temp']
C_temp = converter_of_temperature(K_temp)

feels_like_K = response['main']['feels_like']
feels_like_C = converter_of_temperature(feels_like_K)

K_temp_max = response['main']['temp_max']
C_temp_max = converter_of_temperature(K_temp_max)

K_temp_min = response['main']['temp_min']
C_temp_min = converter_of_temperature(K_temp_min)

```
# More modificated version
```py
import requests
import pprint

API_KEY = "b85d27fc432c0776abd1d268b1320839"
city = input('Enter the name of the city(example: Tashkent or tashkent): ')
exclude = input("Enter an option(current, hourly, daily): ")
response = requests.get(f"https://api.openweathermap.org/data/2.5/weather?q={city}&exclude={exclude}&appid={API_KEY}").json()

pprint.pprint(response, width=100)
Temp = response['main']['temp']

```
# Make a full code of getting data about weather(temp, rain, clouds, wind) hourly, daily, current
