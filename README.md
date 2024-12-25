<h1>Flask To-Do Application</h1>

<h3>Description</h3>
<p>This is a simple To-Do application built with Flask, a Python web framework. It allows users to create, view, update, and delete tasks. The application uses an SQLite database to store tasks and demonstrates the use of Flask routes, templates, and SQLAlchemy for database operations.</p>

<h3>Features</h3>
<ul>
  <li>Add new tasks to the to-do list.</li>
  <li>View all tasks sorted by creation date.</li>
  <li>Update an existing task.</li>
  <li>Delete a task from the list.</li>
</ul>

<h3>Technologies Used</h3>
<ul>
  <li><strong>Python 3.6+</strong></li>
  <li><strong>Flask</strong>: A lightweight web framework for Python.</li>
  <li><strong>Flask-SQLAlchemy</strong>: An ORM (Object Relational Mapper) for database interactions.</li>
  <li><strong>HTML/CSS</strong>: For the front-end templates.</li>
  <li><strong>SQLite</strong>: A lightweight database engine.</li>
</ul>

<h3>Prerequisites</h3>
<p>Before you can run this project, ensure you have the following installed:</p>
<ul>
  <li>Python 3.6 or higher.</li>
  <li>pip (Python package manager).</li>
</ul>

<h3>Installation and Setup</h3>
<p>Follow these steps to run the project on your local machine:</p>


### 1. Clone the Repository
```bash
$ git clone https://github.com/your-username/flask-todo-app.git
$ cd flask-todo-app
```

### 2. Set up a Virtual Environment (Optional but Recommended)
```bash
$ python3 -m venv venv
$ source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Required Dependencies
Install the dependencies listed in the `requirements.txt` file:
```bash
$ pip install -r requirements.txt
```

### 4. Run the Application
Run the Flask app:
```bash
$ python app.py
```

The application will start on `http://127.0.0.1:5000/`.

### 5. Access the Application
Open your web browser and navigate to:
```
http://127.0.0.1:5000/
```
File Structure
```
flask-todo-app/
|-- templates/
|   |-- index.html
|   |-- update.html
|-- app.py
|-- requirements.txt
|-- README.md
|-- venv/ (optional)
```
Templates
- `index.html`: The main page to view and add tasks.
- `update.html`: The page to update an existing task.
`app.py`
The main application file containing Flask routes and logic for CRUD operations.
How to Use the Application
1. Add a task by typing into the input field and submitting it.
2. View all tasks listed on the main page.
3. Update a task by clicking the "Update" button next to it.
4. Delete a task by clicking the "Delete" button next to it.
Required Imports
Ensure the following Python packages are installed:
```python
from flask import Flask, render_template, url_for, request, redirect
from flask_sqlalchemy import SQLAlchemy
from datetime import datetime
```
Dependencies
These dependencies are listed in the `requirements.txt` file:
```
Flask==2.x.x
Flask-SQLAlchemy==2.x.x
```

You can generate this file by running:
```bash
$ pip freeze > requirements.txt
```
Contributing
Feel free to fork this repository, make changes, and submit a pull request. All contributions are welcome!
Acknowledgments
- Flask Documentation: https://flask.palletsprojects.com/
- SQLAlchemy Documentation: https://www.sqlalchemy.org/

Enjoy building your to-do list with Flask!
