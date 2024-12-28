# Ex.08 Design of Interactive Image Gallery
## Date: 28/12/2024

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GALLERY</title>
    <style>
        body {
            background-color: #222;
            font-family: 'Open Sans', sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
        }

        .header {
            text-align: center;
            color: rgb(218, 249, 38);
            font-size: 24px;
            font-weight: bold;
            margin-bottom: 20px;
            font-family: 'Times New Roman', Times, serif;
        }

        .gallery-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 15px;
            padding: 20px;
            max-width: 1200px;
            width: 100%;
            animation: fadeIn 1s ease-in-out;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 10px;
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        }

        .gallery-item img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            transition: transform 0.3s ease, filter 0.3s ease;
        }

        .gallery-item img:hover {
            transform: scale(1.1);
            filter: brightness(0.8);
            cursor: pointer;
        }

        .caption {
            position: absolute;
            bottom: 8px;
            left: 8px;
            background-color: rgba(0, 0, 0, 0.7);
            color: rgb(64, 227, 248);
            padding: 4px 8px;
            border-radius: 4px;
            font-size: 12px;
            text-align: center;
            width: calc(100% - 16px);
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            align-items: center;
            justify-content: center;
        }

        .modal-content {
            margin: auto;
            display: block;
            width: 80%;
            max-width: 600px;
            border-radius: 10px;
        }

        .close {
            position: absolute;
            top: 10px;
            right: 20px;
            color: white;
            font-size: 30px;
            cursor: pointer;
        }

        .modal-description {
            color: white;
            text-align: center;
            padding: 10px;
            font-size: 16px;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .footer{
            font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
            color: rgb(218, 243, 56);
            align-items: end;
            font-size:large;

        }
    </style>
</head>
<body>

    <div class="header">FAMOUS TEMPLE</div>

    <div class="gallery-container">
        <div class="gallery-item">
            <img src="image 6.jpg">
            <div class="caption">ESHA</div>
        </div>
        <div class="gallery-item">
            <img src="img 1.jpg">
            <div class="caption">THANJAVUR</div>
        </div>
        <div class="gallery-item">
            <img src="image 9.jpg">
            <div class="caption">MADURAI MEENAKSHI</div>
        </div>
        <div class="gallery-item">
            <img src="image  2.jpg">
            <div class="caption">VELLORE</div>
        </div>
        <div class="gallery-item">
            <img src="image 5.png">
            <div class="caption">THIRUPATHI</div>
        </div>
    </div>

    <div class="modal" id="modal">
        <span class="close" id="close">&times;</span>
        <img class="modal-content" id="modal-img">
        <div class="modal-description" id="modal-description"></div>
    </div>

    <script>
        const images = document.querySelectorAll('.gallery-item img');
        const modal = document.getElementById('modal');
        const modalImg = document.getElementById('modal-img');
        const modalDescription = document.getElementById('modal-description');
        const closeBtn = document.getElementById('close');

        images.forEach((image) => {
            image.addEventListener('click', () => {
                modal.style.display = 'flex';
                modalImg.src = image.src;
                modalDescription.textContent = image.getAttribute('data-description');
            });
        });

        closeBtn.addEventListener('click', () => {
            modal.style.display = 'none';
        });
    </script>
    <footer>
        <div class="footer">
        <p>Designed and developed by SINDHUJA K </p>
    </div>
    </footer>
</body>
</html>
```

## OUTPUT:
![alt text](<sindhu/gallapp/static/Screenshot (61).png>)
![alt text](<sindhu/gallapp/static/Screenshot (62).png>)
![alt text](<sindhu/gallapp/static/Screenshot (63).png>)
![alt text](<sindhu/gallapp/static/Screenshot (64).png>)
![alt text](<sindhu/gallapp/static/Screenshot (65).png>)
![alt text](<sindhu/gallapp/static/Screenshot (66).png>)




## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
