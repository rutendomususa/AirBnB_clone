# **AirBnB Clone - The Console**

## **Description**

Welcome to the first step of the AirBnB clone project! This project aims to build a command-line interface (CLI) tool that allows users to manage AirBnB objects, including Users, States, Cities, Places, and more. This CLI tool, also referred to as the **console**, is a foundational part of the broader AirBnB clone project, which will eventually include a web application with database integration, APIs, and front-end elements.

---

## **Command Interpreter**

The command interpreter serves as a limited shell for interacting with AirBnB objects. It allows users to perform the following actions:

- **Create objects** (e.g., `User`, `Place`)
- **Retrieve objects** from storage
- **Update object attributes**
- **Delete objects**
- **Display statistics** about objects

---

## **Features**

The console supports the following commands:

### **Core Commands**
| Command                                 | Description                                                  | Example                                           |
|-----------------------------------------|--------------------------------------------------------------|---------------------------------------------------|
| `create <class_name>`                   | Creates a new object and saves it to the storage.            | `create User`                                     |
| `show <class_name> <id>`                | Retrieves an object by its class and unique ID.              | `show User 1234-5678-9101`                       |
| `all [<class_name>]`                    | Displays all objects or objects of a specific class.         | `all User`                                       |
| `update <class_name> <id> <attr> <val>` | Updates an object’s attribute with a new value.              | `update User 1234-5678-9101 name "John Doe"`     |
| `destroy <class_name> <id>`             | Deletes an object by its class and unique ID.                | `destroy User 1234-5678-9101`                    |
| `quit` or `EOF`                         | Exits the console.                                            | `quit`                                           |

---

## **How to Start**

### **Installation**
Ensure you have **Python 3.x** installed on your system.

1. Clone the repository:
   ```bash
   git clone https://github.com/<your-repo-name>.git
   ```
2. Navigate to the project directory:
   ```bash
   cd AirBnB_clone
   ```

### **Starting the Console**
To launch the interactive console:
```bash
./console.py
```

---

## **Examples**

### Interactive Mode
```bash
$ ./console.py
(hbnb) create User
<new_object_id>
(hbnb) all User
[<User object details>]
(hbnb) quit
$
```

### Non-Interactive Mode
You can pass commands directly via a pipe:
```bash
echo "create User" | ./console.py
```

---

## **Project Structure**

```
.
├── README.md
├── AUTHORS
├── console.py
├── models/
│   ├── __init__.py
│   ├── base_model.py
│   ├── user.py
│   ├── state.py
│   ├── city.py
│   ├── place.py
│   └── engine/
│       ├── __init__.py
│       └── file_storage.py
├── tests/
│   ├── test_models/
│   │   ├── test_base_model.py
│   │   ├── test_user.py
│   │   └── ...
│   └── test_engine/
│       └── test_file_storage.py
```

### Key Modules:
- **`console.py`**: The command interpreter.
- **`models/base_model.py`**: Parent class for all models.
- **`models/engine/file_storage.py`**: Handles object storage in a JSON file.
- **`models/`**: Contains all model definitions (e.g., User, State, City, etc.).
- **`tests/`**: Contains unit tests for all modules.

---

## **Unit Testing**

This project includes unit tests to ensure reliability. Tests are located in the `tests/` directory. To run all tests:
```bash
python3 -m unittest discover tests
```

---

## **Authors**

- [Rutendo Kenita Mususa](mailto:ruemususa6700@gmail.com)


---

## **License**

Public Domain.

---

Feel free to update the sections with your specific project details! Let me know if you’d like help customizing it further.
