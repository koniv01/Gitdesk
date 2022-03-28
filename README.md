# Project Name

Software Engineering excersise

## Description

Retrieve data from third party source

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
- Pytest

##### Fetching data from 3rd party source using API
Links:'https://randomuser.me/api'
	  'http://randomfox.ca/floof'

#### Fetching data from API using Pycharm

Because there are some module not available one needs to import the module name or install using 'pip install response on terminal' to avoid text errors.

Once imported we can go ahead and source data from the link above:

import requests

- response = requests.get('https://randomuser.me/api')

- print(response.status_code) this will confirm status by OK or 200

@Run on terminal - Python main.py

- print (response.text) to view the returned text 

- print(response.json()) will print the data returned from the api

- gender = response.json()['results'][0]['gender']- to get the gender,create a gender variable
- print(gender)

- title = response.json()['results'][0]['name']['title']

- first_name = response.json()['results'][0]['name']['first']

- last_name = response.json()['results'][0]['name']['last']

- age = response.json()['results'][0]['dob']['age']
- print(f'{first_name}{last_name}')

- @name variable to access different info:

###### Point* Used the same coding/variables to get the image from URL:'http:randomfox.ca/floof'

- print(response.text) to view the data/value
- fox = response.json()
- print(fox['image']) returned a string linked to image
--------------------------------------------------------------------------------------------------------
###### Also used sqlite3 to get similar data but this time the aim was to persist data and  values as it is a customer database

- import sqlite3

- conn = sqlite3.connect('customer.db')
- c = conn.cursor()
- c.execute("""CREATE TABLE customers (
		first_name text,
		last_name text,
		email text
		)""")
		conn.commit() to execute
- @To insert data into the database table
- c.execute("INSERT INTO customers VALUES('Koni','Muthelo','koni@akeelah.com')")
			Run@python database.py
- many_customers = [
					('Toto','Rams','toto@pila.com'),
					('Tk','Tax','Tk@shiner.com'),
					('Mungu','Nyums','Mungu@rise.com'),
					('Ewart','Leya','Ewart@counted.com'),
					('Tony','Renda','Tony@mashpe.com')
					]
- c.executemany("INSERT INTO customers VALUES (?,?,?,?,?)",)

- c.execute("SELECT * FROM customers")

		print(c.fetchall())
							Run@Sublime Text


- conn.commit()

- conn.close()






 
