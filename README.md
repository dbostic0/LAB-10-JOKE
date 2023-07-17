# LAB-10-JOKE
API JOKE
import requests

url = "https://icanhazdadjoke.com/"

headers = {
    "Accept": "application/json"
}

response = requests.get(url, headers=headers)

if response.status_code == 200:
    data = response.json()
    joke = data["joke"]
    print("Here's a random joke for you:")
    print(joke)
else:
    print("Failed to retrieve a joke. Status code:", response.status_code)
