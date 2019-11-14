# AirBnB_clone
This is a simplified console for the back-end of the AirBnB Clone project.
It is the first step in creating a full AirBnB Clone. This AirBnB_clone repository was created by BrandynReindel and Gareth Brickman.
### Repository Contents
The repository contains the following files:
|   **File**    |  **Decription**                       |
|---------------|---------------------------------------|
| console.py   | entry point of the command interpreter           |
| init_test.sh      | executes all the test files from tests folder        |
| models/__init__.py | creates an instance of FileStorage |
| models/amenity.py | class Amenity, inherits from BaseModel |
| models/base_model.py | class BaseModel that defines all common attributes/methods for other classes |
| models/city.py | class City, inherits from BaseModel |
| models/place.py | class Place, inherits from BaseModel |
| models/review.py | class Review, inherits from BaseModel |
| models/state.py | class State, inherits from BaseModel |
| models/user.py | class User, inherits from BaseModel |
| models/engine/file_storage.py | class FileStorage, serializes instances to a JSON file and deserializes JSON file to instances |
| tests/test_models/amenity_test.py | tests Amenity class |
| tests/test_models/basemodel_test.py | tests BaseModel class |
| tests/test_models/city_test.py | tests City class |
| tests/test_models/place_test.py | tests Place class |
| tests/test_models/review_test.py | tests Review class |
| tests/test_models/state_test.py | tests State class |
| tests/test_models/user_test.py | tests User class |
### Installation
-   Clone this repository:  `git clone "https://github.com/brandynr/AirBnB_clone.git"`
-   Access AirBnb directory:  `cd AirBnB_clone`
-
### Usage
-   Run hbnb(interactively):
```python
$ ./console.py
(hbnb) help
Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb)
(hbnb)
(hbnb) quit
$
```
-   Run hbnb(non-interactively):
```python
$ echo "help" | ./console.py
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
$
```
### Console Commands
console.py - the console contains the entry point of the command interpreter. List of commands this console supports:
-   `quit`  - exits console
-   `create`  - Creates a new instance of`BaseModel`, saves it (to the JSON file) and prints the id
-   `destroy`  - Deletes an instance based on the class name and id (save the change into the JSON file).
-   `show`  - Prints the string representation of an instance based on the class name and id.
-   `all`  - Prints all string representation of all instances based or not on the class name.
-   `update`  - Updates an instance based on the class name and id by adding or updating attribute (save the change into the JSON file).
### Examples
```python
$ ./console.py
(hbnb) show BaseModel
** instance id missing **
(hbnb) show BaseModel Holberton
** no instance found **
(hbnb) create BaseModel
49faff9a-6318-451f-87b6-910505c55907
(hbnb) all BaseModel
["[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'id': '49faff9a-6318-451f-87b6-910505c55907', 'updated_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903300)}"]
(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907
[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'id': '49faff9a-6318-451f-87b6-910505c55907', 'updated_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903300)}
(hbnb) destroy
** class name missing **
(hbnb) update BaseModel 49faff9a-6318-451f-87b6-910505c55907 first_name "Betty"
(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907
[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'first_name': 'Betty', 'id': '49faff9a-6318-451f-87b6-910505c55907', 'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 3, 49401)}
(hbnb) create BaseModel
2dd6ef5c-467c-4f82-9521-a772ea7d84e9
(hbnb) all BaseModel
["[BaseModel] (2dd6ef5c-467c-4f82-9521-a772ea7d84e9) {'id': '2dd6ef5c-467c-4f82-9521-a772ea7d84e9', 'created_at': datetime.datetime(2017, 10, 2, 3, 11, 23, 639717), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 23, 639724)}", "[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'first_name': 'Betty', 'id': '49faff9a-6318-451f-87b6-910505c55907', 'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 3, 49401)}"]
(hbnb) destroy BaseModel 49faff9a-6318-451f-87b6-910505c55907
(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907
** no instance found **
(hbnb)
```
### Contributing
Any pull requests for adding features or fixing bugs will be manually reviewed. Please see the AUTHORS file for contact information.
