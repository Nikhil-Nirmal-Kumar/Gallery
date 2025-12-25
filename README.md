# Ex.08 Design of Interactive Image Gallery
# Date:
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
image.html

<!DOCTYPE html>
<html lang="en">
<head>
    <title>Fancy Interactive Image Gallery</title>
    <style>
        body {
            margin: 0;
            font-family: 'Segoe UI', sans-serif;
            background: linear-gradient(135deg, #667eea, #764ba2);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .container {
            width: 90%;
            max-width: 1000px;
            padding: 30px;
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(12px);
            border-radius: 25px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.3);
        }

        h2 {
            color: white;
            text-align: center;
            margin-bottom: 30px;
            letter-spacing: 2px;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }

        .card {
            position: relative;
            overflow: hidden;
            border-radius: 18px;
            cursor: pointer;
            transition: transform 0.4s ease;
        }

        .card:hover {
            transform: translateY(-8px);
        }

        .card img {
            width: 100%;
            height: 230px;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .card:hover img {
            transform: scale(1.1);
        }

        .overlay {
            position: absolute;
            inset: 0;
            background: linear-gradient(to top, rgba(0,0,0,0.7), transparent);
            opacity: 0;
            transition: opacity 0.4s ease;
            display: flex;
            align-items: flex-end;
            padding: 15px;
            color: white;
            font-size: 16px;
            font-weight: 600;
        }

        .card:hover .overlay {
            opacity: 1;
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            inset: 0;
            background: rgba(0,0,0,0.85);
            justify-content: center;
            align-items: center;
            z-index: 10;
        }

        .modal img {
            max-width: 90%;
            max-height: 85%;
            border-radius: 20px;
            animation: zoom 0.4s ease;
        }

        @keyframes zoom {
            from { transform: scale(0.6); opacity: 0; }
            to { transform: scale(1); opacity: 1; }
        }

        .close {
            position: absolute;
            top: 25px;
            right: 40px;
            color: white;
            font-size: 35px;
            cursor: pointer;
        }
    </style>
</head>
<body>

<div class="container">
    <h2>Interactive Image Gallery</h2>

    <div class="gallery">
        <div class="card" onclick="openModal('img1.webp')">
            <img src="img1.webp">
            <div class="overlay">Nature View</div>
        </div>

        <div class="card" onclick="openModal('img2.webp')">
            <img src="img2.webp">
            <div class="overlay">Aurora Lights</div>
        </div>

        <div class="card" onclick="openModal('img3.webp')">
            <img src="img3.webp">
            <div class="overlay">Mountain Peaks with a Lakeside View</div>
        </div>

        <div class="card" onclick="openModal('img4.webp')">
            <img src="img4.webp">
            <div class="overlay">The Hills</div>
        </div>

        <div class="card" onclick="openModal('img5.webp')">
            <img src="img5.webp">
            <div class="overlay">Ocean Housing</div>
        </div>

        <div class="card" onclick="openModal('img6.webp')">
            <img src="img6.webp">
            <div class="overlay">Village on a Cliff</div>
        </div>

        <div class="card" onclick="openModal('img7.webp')">
            <img src="img7.webp">
            <div class="overlay">Beautiful Lake</div>
        </div>

        <div class="card" onclick="openModal('img8.webp')">
            <img src="img8.webp">
            <div class="overlay">Beautiful City Bridge</div>
        </div>
    </div>
</div>

<!-- Modal -->
<div class="modal" id="imageModal" onclick="closeModal()">
    <span class="close">&times;</span>
    <img id="modalImage">
</div>

<script>
    function openModal(src) {
        document.getElementById("modalImage").src = src;
        document.getElementById("imageModal").style.display = "flex";
    }

    function closeModal() {
        document.getElementById("imageModal").style.display = "none";
    }
</script>

</body>
</html>
```
# OUTPUT:
<img width="1920" height="1080" alt="Screenshot (63)" src="https://github.com/user-attachments/assets/7b6b199e-cde1-4001-8201-6b520924f623" />
<img width="1920" height="1080" alt="Screenshot (64)" src="https://github.com/user-attachments/assets/639f3acd-eec4-4ec1-be91-0df3f1555422" />
<img width="1920" height="1080" alt="Screenshot (65)" src="https://github.com/user-attachments/assets/f6f9c11f-9807-4fa2-8e55-cfb8ea43548f" />

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
