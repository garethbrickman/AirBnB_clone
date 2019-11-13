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
* Clone this repository: `git clone "https://github.com/brandynr/AirBnB_clone.git"`
* Access AirBnb directory: `cd AirBnB_clone`
* Run hbnb(interactively): `./console` and enter command
* Run hbnb(non-interactively): `echo "<command>" | ./console.py`

### Console Commands
[console.py](console.py) - the console contains the entry point of the command interpreter. 
List of commands this console supports:
* `EOF` - exits console
* `quit` - exits console
* `<emptyline>` - overwrites default emptyline method and does nothing
* `create` - Creates a new instance of`BaseModel`, saves it (to the JSON file) and prints the id
* `destroy` - Deletes an instance based on the class name and id (save the change into the JSON file). 
* `show` - Prints the string representation of an instance based on the class name and id.
* `all` - Prints all string representation of all instances based or not on the class name. 
* `update` - Updates an instance based on the class name and id by adding or updating attribute (save the change into the JSON file). 

### Example


