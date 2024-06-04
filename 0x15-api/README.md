# 0x15-API

## Introduction

This repository contains Python scripts that demonstrate how to interact with APIs (Application Programming Interfaces) to gather data from external sources, export data to different file formats, and manipulate data in various ways.

## Scripts

### 0-gather_data_from_an_API.py

**Usage:**
```
$ ./0-gather_data_from_an_API.py <user_id>
```

**Description:**
This script retrieves information about a given user's TODO list from the JSONPlaceholder API (https://jsonplaceholder.typicode.com/). It displays the employee's name, the number of tasks completed, and the titles of the completed tasks.

**Parameters:**
- `<user_id>`: The numerical ID of the user whose TODO list you want to retrieve.

### 1-export_to_CSV.py

**Usage:**
```
$ ./1-export_to_CSV.py <user_id>
```

**Description:**
This script exports the TODO list of a specified user to a CSV (Comma-Separated Values) file. It retrieves the user's data from the JSONPlaceholder API and writes it to a CSV file named `<user_id>.csv`.

**Parameters:**
- `<user_id>`: The numerical ID of the user whose TODO list you want to export.

### 2-export_to_JSON.py

**Usage:**
```
$ ./2-export_to_JSON.py <user_id>
```

**Description:**
This script exports the TODO list of a specified user to a JSON (JavaScript Object Notation) file. It retrieves the user's data from the JSONPlaceholder API and writes it to a JSON file named `<user_id>.json`.

**Parameters:**
- `<user_id>`: The numerical ID of the user whose TODO list you want to export.

### 3-dictionary_of_list_of_dictionaries.py

**Usage:**
```
$ ./3-dictionary_of_list_of_dictionaries.py
```

**Description:**
This script exports the TODO list of all users to a JSON file. It retrieves data for all users from the JSONPlaceholder API, organizes it into a dictionary of lists of dictionaries, and then writes it to a JSON file named `todo_all_employees.json`.

## License

Licensed to ALX - Holberton School

## Authors

- Precious Okwukwe Amaechi
