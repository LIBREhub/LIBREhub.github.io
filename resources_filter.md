---
title: Resources
permalink: /resources_filter/
---
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Blog Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
        }
        #filters {
            margin-bottom: 20px;
        }
        .filter-button {
            padding: 10px 15px;
            margin: 5px;
            cursor: pointer;
            border: none;
            background-color: #007BFF;
            color: white;
            border-radius: 5px;
        }
        .filter-button.active {
            background-color: #0056b3;
        }
        #blog-posts {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }
        .post {
            border: 1px solid #ccc;
            padding: 10px;
            border-radius: 5px;
            box-shadow: 2px 2px 5px rgba(0,0,0,0.1);
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div id="filters">
        <button class="filter-button active" data-category="all">All</button>
        <button class="filter-button" data-category="category1">Category 1</button>
        <button class="filter-button" data-category="category2">Category 2</button>
        <!-- Add more buttons for categories as needed -->
    </div>
    <div id="blog-posts">
        <!-- Blog posts will be loaded here dynamically -->
    </div>
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            var filterButtons = document.querySelectorAll('.filter-button');
            var postsContainer = document.getElementById('blog-posts');
            
            // Function to fetch and display posts
            function fetchAndDisplayPosts(category) {
                fetch('posts.json')
                    .then(response => response.json())
                    .then(posts => {
                        postsContainer.innerHTML = ''; // Clear previous posts
                        posts.forEach(post => {
                            if (category === 'all' || post.category === category) {
                                var postElement = document.createElement('div');
                                postElement.classList.add('post');
                                postElement.setAttribute('data-category', post.category);
                                postElement.innerHTML = `
                                    <h2>${post.title}</h2>
                                    <p>${post.content}</p>
                                `;
                                postsContainer.appendChild(postElement);
                            }
                        });
                    });
            }
            
            // Initial fetch and display all posts
            fetchAndDisplayPosts('all');

            filterButtons.forEach(function(button) {
                button.addEventListener('click', function() {
                    // Remove active class from all buttons
                    filterButtons.forEach(function(btn) {
                        btn.classList.remove('active');
                    });

                    // Add active class to the clicked button
                    button.classList.add('active');

                    // Fetch and display posts based on selected category
                    var selectedCategory = button.getAttribute('data-category');
                    fetchAndDisplayPosts(selectedCategory);
                });
            });
        });
    </script>
</body>
</html>