<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Library Management System</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 20px;
        }

        .container {
            max-width: 600px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        h1, h2 {
            text-align: center;
        }

        form {
            display: flex;
            flex-direction: column;
        }

        input {
            margin: 10px 0;
            padding: 10px;
        }

        button {
            padding: 10px;
            background-color: #28a745;
            color: white;
            border: none;
            cursor: pointer;
        }

        button:hover {
            background-color: #218838;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Library Management System</h1>
        <form id="bookForm">
            <input type="text" id="title" placeholder="Book Title" required>
            <input type="text" id="author" placeholder="Author" required>
            <input type="text" id="isbn" placeholder="ISBN" required>
            <button type="submit">Add Book</button>
        </form>
        <h2>Book List</h2>
        <ul id="bookList"></ul>
    </div>
    <script>
        document.getElementById('bookForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const title = document.getElementById('title').value;
            const author = document.getElementById('author').value;
            const isbn = document.getElementById('isbn').value;

            const bookList = document.getElementById('bookList');
            const li = document.createElement('li');
            li.textContent = `Title: ${title}, Author: ${author}, ISBN: ${isbn}`;
            bookList.appendChild(li);

            // Clear the form
            document.getElementById('bookForm').reset();
        });
    </script>
</body>
</html>
