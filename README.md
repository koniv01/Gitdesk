# Project Name

Software Engineering excersise

## Description

Sweepstars employees are struggling to get retrieve data from third party source

### Table of contents
This will be used to reference the location of destination

- [Description](#Description)
- [How To Use](#how-to-use)
- [References](#references)
- [License](#Licence)
- [Author info](#author-info)

#### Technologies

- Python/Pycharm
- Sublime text
- Github desktop
- GitBash

##### Fetching data from 3rd party source using API
Links:'https://randomuser.me/api'
	  'http://randomfox.ca/floof'

#### Fetching data from API using Pycharm

Because there are some module not available one needs to import the module name or install using 'pip install response on terminal' to avoid text errors.

Once imported we can go ahead and source data from the link above:

import requests

response = requests.get('https://randomuser.me/api')
print(response.status_code) this will confirm status by OK or 200
print(response.json())

gender = response.json()['results'][0]['gender']
print(gender)

title = response.json()['results'][0]['name']['title']

first_name = response.json()['results'][0]['name']['first']

last_name = response.json()['results'][0]['name']['last']

age = response.json()['results'][0]['dob']['age']

print(f'{first_name}{last_name}')
print(f'Age: {age}')

###### the data sourced will be returned with information for each group after running the code in question e.g gender,name ,email adress,value etc






 
