![logo](/logo.png)
# AirBnB clone - The console

This is the console /command interpreter for the Holberton Airbnb clone project. The console can be used to store objects in and retrieve objects from a JSON.

* Implement cmd module
* Implement uuid module
* Implement datetime
* Unittest module
---
## Install

```
git clone https://github.com/JuanJoseGomezR/AirBnB_clone.git
cd AirBnB_clone/
```
---

## Usage of command interpreter
Interactive Mode:
1. Run program and show prompt with help command.
```sh
PROMPT~> ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb)
(hbnb) help quit
Quit command to exit the program

(hbnb)
(hbnb)
(hbnb) quit
PROMPT~>
```
Non-interactive Mode:
1. Run the following command: echo "help" | ./console.py
```sh
(hbnb)
Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
```
---
## CMD Commands

| Command | Description | Sample Usage
| --- | --- | --- |
| Help | Show all available commands | help  |
| Quit | Exit to the prompt | quit |
| Create | Create a new object | create class |
| Show | Retrieve an object from a file | show class name id |
| All | Display all objects in class | all class |
| Update | Update objects and attributes | update class id name key |
| Destroy | Destroy specified object | destroy class |

---
## Usage EOF:
With the EOF command, you exit the console.
```sh
(hbnb)EOF
vagrant@vagrant-ubuntu-trusty-64:~/AirBnB_clone$
```
## Usage Quit:
With the quit command, you exit the console.
```sh
(hbnb)quit
vagrant@vagrant-ubuntu-trusty-64:~/AirBnB_clone$
```
## Usage Create:
With the create command, a new instance of BaseModel is created and it is save to the JSON file, then it prints the instance id.
```sh
(hbnb) create BaseModel
d4f9b14b-7afc-466c-8f55-5c154c8ffa35
```
## Usage All:
With the all command, all instances are displayed, returning a serialized json (string).

```sh
(hbnb) all BaseModel
["[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'id': '49faff9a-6318-451f-87b6-910505c55907', 'updated_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903300)}"]

```
 ## Usage Show:
With the show command, the instance is displayed, returning a dictionary of the id instance.

```sh
show BaseModel 49faff9a-6318-451f-87b6-910505c55907
[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'id': '49faff9a-6318-451f-87b6-910505c55907', 'updated_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903300)}

 ```
## Usage Update:
With the update command, the attributes of the instances are updated.

```sh
(hbnb) update BaseModel 49faff9a-6318-451f-87b6-910505c55907 first_name "Betty"
(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907
[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'first_name': 'Betty', 'id': '49faff9a-6318-451f-87b6-910505c55907', 'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 3, 49401)}

```

## Usage Destroy:
With the Destroy command, instances are destroyed.

```sh
(hbnb) destroy BaseModel 49faff9a-6318-451f-87b6-910505c55907
(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907
** no instance found **
(hbnb) 
```
---
## Authors:
* [Juan Gómez](https://twitter.com/J_Gmez)
* [Ricky Mosquera](https://twitter.com/MosqueraR98)