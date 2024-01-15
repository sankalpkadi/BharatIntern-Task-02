# BharatIntern-Task-02
# using HTML
<!DOCTYPE html>
<html>
<head>
    <title>My Blog</title>
    <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
    <header>
        <h1>Welcome to My Blog</h1>
    </header>
    
    <nav>
        <ul>
            <li><a href="/">Home</a></li>
            <li><a href="/posts">Posts</a></li>
            <li><a href="/create">Create Post</a></li>
        </ul>
    </nav>
    
    <main>
        <!-- Content goes here -->
    </main>
    
    <footer>
        <p>&copy; 2022 My Blog. All rights reserved.</p>
    </footer>
</body>
</html>

#using CSS
/* style.css */

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: #fff;
    padding: 20px;
}

nav {
    background-color: #f2f2f2;
    padding: 10px;
}

nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

nav ul li {
    display: inline;
    margin-right: 10px;
}

nav ul li a {
    text-decoration: none;
    color: #333;
}

main {
    padding: 20px;
}

footer {
    background-color: #333;
    color: #fff;
    padding: 10px;
    text-align: center;
}

#using node.js in mangodb
// server.js

const express = require('express');
const app = express();
const port = 3000;

// Routes
app.get('/', (req, res) => {
    res.sendFile(__dirname + '/index.html');
});

app.get('/posts', (req, res) => {
    // Logic to fetch and display posts from MongoDB
});

app.get('/create', (req, res) => {
    // Logic to create a new post and save it to MongoDB
});

// Start the server
app.listen(port, () => {
    console.log(`Server running on port ${port}`);
});
// db.js

const mongoose = require('mongoose');

mongoose.connect('mongodb://localhost/blog', {
    useNewUrlParser: true,
    useUnifiedTopology: true
}).then(() => {
    console.log('Connected to MongoDB');
}).catch((error) => {
    console.error('Error connecting to MongoDB:', error);
});
