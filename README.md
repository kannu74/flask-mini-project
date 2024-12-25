<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flask To-Do App</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }
        .container {
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 20px;
            width: 100%;
            max-width: 600px;
        }
        h1 {
            text-align: center;
            color: #333;
        }
        form {
            display: flex;
            margin-bottom: 20px;
        }
        input[type="text"] {
            flex: 1;
            padding: 10px;
            font-size: 16px;
            border: 1px solid #ccc;
            border-radius: 4px;
            margin-right: 10px;
        }
        button {
            background-color: #28a745;
            color: white;
            border: none;
            padding: 10px 15px;
            font-size: 16px;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #218838;
        }
        ul {
            list-style-type: none;
            padding: 0;
        }
        li {
            background: #f9f9f9;
            margin: 5px 0;
            padding: 10px;
            border-radius: 4px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .actions {
            display: flex;
            gap: 10px;
        }
        .actions a {
            text-decoration: none;
            color: #fff;
            padding: 5px 10px;
            border-radius: 4px;
        }
        .actions .update {
            background-color: #007bff;
        }
        .actions .delete {
            background-color: #dc3545;
        }
        .actions a:hover {
            opacity: 0.9;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>To-Do List</h1>
        <form method="POST" action="/">
            <input type="text" name="content" placeholder="Enter a new task" required>
            <button type="submit">Add Task</button>
        </form>
        <ul>
            {% for task in tasks %}
            <li>
                <span>{{ task.content }}</span>
                <div class="actions">
                    <a href="/update/{{ task.id }}" class="update">Update</a>
                    <a href="/delete/{{ task.id }}" class="delete">Delete</a>
                </div>
            </li>
            {% endfor %}
        </ul>
    </div>
</body>
</html>
