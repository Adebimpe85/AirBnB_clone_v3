"AirBnB clone v3
# AirBnB Clone v3

![AirBnB Clone Logo](link-to-your-logo)

The AirBnB Clone v3 project is a command-line interface that serves as the first segment of the AirBnB project at Holberton School. The goal of this project is to create a simplified copy of the AirBnB website (HBnB) by implementing fundamental concepts of higher-level programming. The command interpreter included in this segment allows for the management of objects related to the AirBnB(HBnB) website.

## Functionalities

The command interpreter provides the following functionalities:

- Create a new object (e.g., User, Place)
- Retrieve an object from a file, database, etc.
- Perform operations on objects (count, compute stats, etc.)
- Update attributes of an object
- Destroy an object

## Environment

This project is interpreted and tested on Ubuntu 14.04 LTS using Python 3 (version 3.4.3).

## Installation

To get started with the AirBnB Clone v3 project, follow these steps:

1. Clone this repository: `git clone https://github.com/ehoneahobed/AirBnB_clone_v3.git`
2. Access the AirBnB directory: `cd AirBnB_clone_v3`
3. Run the console interactively: `./console.py` and enter commands
4. Run the console non-interactively: `echo "<command>" | ./console.py`

## File Descriptions

- `console.py`: The console serves as the entry point of the command interpreter. It supports the following commands:
    - `EOF`: Exits the console
    - `quit`: Exits the console
    - `<emptyline>`: Overwrites the default emptyline method and does nothing
    - `create`: Creates a new instance of BaseModel, saves it (to the JSON file), and prints the ID
    - `destroy`: Deletes an instance based on the class name and ID (saves the change into the JSON file)
    - `show`: Prints the string representation of an instance based on the class name and ID
    - `all`: Prints the string representation of all instances based on the class name
    - `update`: Updates an instance based on the class name and ID by adding or updating an attribute (saves the change into the JSON file)

- `models/` directory: Contains classes used in this project
    - `base_model.py`: The BaseModel class from which future classes will be derived
        - `__init__(self, *args, **kwargs)`: Initialization of the base model
        - `__str__(self)`: String representation of the BaseModel class
        - `save(self)`: Updates the attribute `updated_at` with the current datetime
        - `to_dict(self)`: Returns a dictionary containing all keys/values of the instance

    Classes inherited from BaseModel:
    - `amenity.py`
    - `city.py`
    - `place.py`
    - `review.py`
    - `state.py`
    - `user.py`

- `models/engine/` directory: Contains the File Storage class that handles JSON serialization and deserialization
    - `file_storage.py`: Serializes instances to a JSON file and deserializes back to instances
        - `all(self)`: Returns the dictionary `__objects`
        - `new(self, obj)`: Sets the `obj` with key `.id` in `__objects`
        - `save(self)`: Serializes `__objects` to the JSON file (path:
"
