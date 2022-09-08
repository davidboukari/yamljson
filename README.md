# yamljson


<img width="1674" alt="image" src="https://user-images.githubusercontent.com/32338685/189145922-bbfb0547-23d4-4ade-b865-aadee2857479.png">

* Yaml converter: https://codebeautify.org/yaml-to-json-xml-csv

```
# This is a comment:  start by '#' Create an object
base_person: &base
  city: New-York
  Country: USA

Person:
  # Use the anchor base person to add the properties to the person
  <<: *base
  name: John
  age: 29
  isMale: true
  #list in yaml
  stuff:
    - laptop
    - car
    - bike
  # Other way to write list
  food: [ pizza, donuts, cake ]
  # Add a list of objects
  friends:
    - name: Jane
      age: 19
    - name: Mike
      age: 22

```
* Convert to yaml
```
{
	"base_person": {
		"city": "New-York",
		"Country": "USA"
	},
	"Person": {
		"city": "New-York",
		"Country": "USA",
		"name": "John",
		"age": 29,
		"isMale": true,
		"stuff": [
			"laptop",
			"car",
			"bike"
		],
		"food": [
			"pizza",
			"donuts",
			"cake"
		],
		"friends": [
			{
				"name": "Jane",
				"age": 19
			},
			{
				"name": "Mike",
				"age": 22
			}
		]
	}
}

```
