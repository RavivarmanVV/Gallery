# Ex.08 Design of Interactive Image Gallery
# Date:15-05-2025
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
HTML

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>BIKE SHOWROOM</h1>
    </header>
    <div class="gallery">
        <div class="gallery-item" onclick="openModal(this)">
            <img src="ninja.jpg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="ns 200.jpg"  >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="gt 650.jpg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="rs457.jpg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="s1000.jpg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="triumph.jpg" >
        </div>
        <div class="gallery-item" onclick="openModal(this)">
            <img src="ducati.jpg" >
        </div>
    </div>

    <div id="modal" class="modal">
        <span class="close" onclick="closeModal()">&times;</span>
        <img class="modal-content" id="modalImage">
        <div id="caption"></div>
    </div>

    <script src="gallery.js"></script>
</body>
</html>
```
```
CSS

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    background-color: #f4f4f4;
    min-height: 100vh;
}

header h1 {
    margin: 40px 0;
    color: #333;
    font-size: 2rem;
    text-align: center;
    font-weight: bold;
    font-family: cursive;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 15px;
    max-width: 90%;
}

.gallery-item {
    overflow: hidden;
    position: relative;
}

.gallery-item img {
    width: 100%;
    height: 150px; /* Fixed height for equal size */
    object-fit: cover; /* Ensures images maintain aspect ratio while filling the space */
    border-radius: 8px;
    cursor: pointer;
    transition: transform 0.3s ease;
}

.gallery-item img:hover {
    transform: scale(1.1);
}

.modal {
    display: none;
    position: fixed;
    z-index: 1000;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    justify-content: center;
    align-items: center;
}

.modal-content {
    max-width: 90%;
    max-height: 80%;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.modal .close {
    position: absolute;
    top: 20px;
    right: 40px;
    color: white;
    font-size: 35px;
    font-weight: bold;
    cursor: pointer;
}

#caption {
    color: white;
    margin-top: 15px;
    text-align: center;
    font-size: 16px;
}
```
```
JAVASRIPT

function openModal(element) {
    const modal = document.getElementById("modal");
    const modalImage = document.getElementById("modalImage");
    const caption = document.getElementById("caption");

    modal.style.display = "flex";
    modalImage.src = element.querySelector("img").src;
    caption.textContent = element.querySelector("img").alt;
}

function closeModal() {
    const modal = document.getElementById("modal");
    modal.style.display = "none";
}
```
# OUTPUT:
![Screenshot 2025-05-18 112452](https://github.com/user-attachments/assets/12bc7360-e698-4b15-8cb2-ae714a8f0c14)
![Screenshot 2025-05-18 112440](https://github.com/user-attachments/assets/f32635a3-1345-4008-b971-ce7e9db7a776)
![Screenshot 2025-05-18 112431](https://github.com/user-attachments/assets/1772c229-451a-411e-bc18-b16859f0b340)
![Screenshot 2025-05-18 112420](https://github.com/user-attachments/assets/93604562-d8c5-42fc-b6e9-4b85e944634e)
![Screenshot 2025-05-18 112231](https://github.com/user-attachments/assets/f11df24a-9afd-49c6-a862-6be0da46b5a7)
![Screenshot 2025-05-18 112221](https://github.com/user-attachments/assets/5aa84900-5c8b-43d5-8731-321b38f24522)
![Screenshot 2025-05-18 112209](https://github.com/user-attachments/assets/d41f7c82-5d7d-4fc8-aa16-14986d99f630)
![Screenshot 2025-05-18 112150](https://github.com/user-attachments/assets/f4c2d1eb-bd30-4d07-a87d-4b6aeb0eea8b)

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
