---
navigation: true
cover: ''
title: Books for Learning Technical Topics
date: 2024-07-14
class: post-template
---

For a long time, I have been gather resources to help me with my goals and projects. Specifically, I have been slowly growing my collection of technical books, from 6th grade to 
the present. And I would like to share them with you here. 

# Book Display

---
layout: default
---

{% raw %}
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Book Display</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background-color: #ffffff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            padding: 20px;
            text-align: center;
            max-width: 400px;
            width: 100%;
        }
        .book-cover {
            max-width: 100%;
            height: auto;
            margin-bottom: 10px;
        }
        .button-container {
            margin-top: 15px;
        }
        .amazon-button {
            background-color: #ff9900;
            color: #ffffff;
            border: none;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            border-radius: 4px;
            text-decoration: none;
            transition: background-color 0.3s ease;
        }
        .amazon-button:hover {
            background-color: #e68a00;
        }
    </style>
</head>
<body>
    <div class="container" id="bookDisplay">
        <h2>Book Display</h2>
        <div id="bookInfo">
            <img class="book-cover" id="bookCover" src="loading.gif" alt="Book Cover">
        </div>
        <div class="button-container">
            <a id="amazonLink" class="amazon-button" href="#" target="_blank">View on Amazon</a>
        </div>
    </div>

    <script>
        // Function to extract ASIN from Amazon URL
        function extractASIN(url) {
            let match = url.match(/\/(dp|gp\/product)\/([0-9A-Z]{10})/);
            return match ? match[2] : null;
        }

        // Function to fetch book information and update display
        function fetchBookInfo(url) {
            let asin = extractASIN(url);
            if (!asin) {
                alert('Invalid Amazon link. Please provide a valid Amazon product page URL.');
                return;
            }

            let amazonApiUrl = `https://www.amazon.com/gp/product/${asin}/?language=en_US&psc=1&sprefix=book`;
            
            fetch(amazonApiUrl)
                .then(response => response.text())
                .then(data => {
                    let parser = new DOMParser();
                    let htmlDoc = parser.parseFromString(data, 'text/html');
                    let bookCover = htmlDoc.querySelector('#imgBlkFront');

                    if (bookCover) {
                        document.getElementById('bookCover').src = bookCover.src;
                        document.getElementById('amazonLink').href = amazonApiUrl;
                    } else {
                        alert('Failed to fetch book information. Please try again later.');
                    }
                })
                .catch(error => {
                    console.error('Error fetching book information:', error);
                    alert('Failed to fetch book information. Please try again later.');
                });
        }

        // Replace with your Amazon link
        let amazonLink = "[https://www.amazon.com/dp/B09FQ48V74](https://www.amazon.com/Practical-Algebra-Self-Teaching-Guide-Second/dp/0471530123/ref=sr_1_4?crid=AEVGNKLDR9WW&dib=eyJ2IjoiMSJ9.ZF6lT-0kmh65KXhCHGSSeqGl0u03zFrfD1ntdNkBZNskkOSH-004pX5ujm4oNeaHENVxd0rq_K7Xo9rHkZwGrbzjSC7nsUWzp_Af0uEbf7ElBNNWeJeBGpGdQRoUF3Fag76NiR9yugDIc4rQ3OBZyeUMG4ugd3xBsFDmNfx8Rvb2zelDI8D-bBpF4EfiKwO4rowYlZMY5e4uL7JkU3xH7TwGdpKCKNmma84IUTemb40.eAb8913vDP9cEoSWcVTNlfuze3WrvVTYh4weSw4PMMY&dib_tag=se&keywords=practical+algebra&qid=1721076656&sprefix=practical%2Caps%2C1541&sr=8-4)";

        // Fetch book information
        fetchBookInfo(amazonLink);
    </script>
</body>
</html>
{% endraw %}
