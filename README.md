AirBnB Clone - Command Interpreter
========================================

Description
This project is the first step towards creating a clone of the popular AirBnB web application. We start by building a command-line interface (CLI) that will allow us to manage different objects in the AirBnB environment. This includes tasks such as creating, modifying, and deleting objects (e.g., User, City, Place) and storing their state in a file.

This command interpreter is crucial as it will be used in future steps to integrate the application with a web interface, a database, and APIs. Our goal is to build a functional, modular application that scales as additional components are added.

Command Interpreter
========================================
The command interpreter acts as a limited-use shell for managing AirBnB objects, following the pattern of:
- Create new objects.
- Retrieve objects from storage.
- Perform operations (count, compute stats).
- Update object attributes.
- Delete objects.

How to Start the Command Interpreter
========================================
Clone the repository: <br>bash <br>Copy code: <br>git clone https://github.com/DavidDau/AirBnB_clone.git

1. Make the console script executable:<br>bash<br>Copy code *chmod +x console.py*

2. Run the command interpreter in interactive mode:<br>bash<br>Copy code *./console.py*


You can also run it in non-interactive mode by echoing commands:<br>bash<br>Copy code *echo "help" | ./console.py*


How to Use the Command Interpreter
========================================
Once inside the command interpreter (in interactive mode), you can run several commands:

<br>**help**: Displays the list of commands or provides help for a specific command.
<br>
bash
<br>
Copy code
<br>
*help*
<br>
*Documented commands (type help ):*
<br>
*EOF  help  quit*

<br>create <class>: Creates a new object of the specified class (e.g., User, City).
<br>
bash
<br>
Copy code
<br>
*create User*


show <class> <id>: Shows the details of a specific object based on its class and ID.
<br>
bash
<br>
Copy code
<br>
*show User 1234-1234-1234*


destroy <class> <id>: Deletes a specified object.
<br>
bash
<br>
Copy code
<br>
*destroy User 1234-1234-1234*


all [<class>]: Shows all objects or all objects of a specific class.
<br>
bash
<br>
Copy code
<br>
*all*
<br>
*all User*
<br>
*update <class> <id> <attribute_name> <attribute_value>: Updates the attributes of a specific object.*
<br>
bash 
<br>
Copy code
<br>
*update User 1234-1234-1234 email "newemail@example.com"*


quit: Exits the command interpreter.

Examples
=========
Interactive mode:
<br>
bash
<br>
Copy code
<br>
*$ ./console.py*
<br>
*help*
<br>
Documented commands (type help <topic>):
<br>
EOF  help  quit
<br>
*create User*
<br>
*1234-5678-9012*
<br>
*show User 1234-5678-9012*

[User] (1234-5678-9012) {'id': '1234-5678-9012', 'created_at': '2024-09-09T00:00:00', ...}
<br>
*quit*
<br>
$

Non-interactive mode:
<br>
bash
<br>
Copy code
<br>
*$ echo "create User" | ./console.py*
<br>
*1234-5678-9012*
<br>
*$*


Project Structure
========================================
The project includes the following key components:<br>
- **BaseModel:** The parent class that handles initialization, serialization, and deserialization of objects.
- **User, State, City, Place, etc.:** Classes that inherit from BaseModel and represent AirBnB entities.
- **FileStorage:** The storage engine that serializes objects to and deserializes objects from a JSON file.
- **Unit Tests:** Located in the tests/ directory to ensure the correct functionality of all components.
