## INTERACTIVE IMAGE GALLERY
# NAME: TARANIKKA A
# REG NO: 212223220115
# DATE: 22/03/25
 
 # PROGRAM:

 # index.html:
 ```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Image Gallery</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <h2>Image Gallery</h2>

    <div class="gallery-container">
        <button id="prevBtn">❮</button>
        <div class="gallery">
            <div class="image">
                <img src="c:\Users\admin\Desktop\1.jpg" alt="TREES">
                <div class="TREES">SKY</div>
            </div>
            <div class="image">
                <img src="c:\Users\admin\Desktop\2.jpg" alt="MOON">
                <div class="MOON">MOON</div>
            </div>
            <div class="image">
                <img src="c:\Users\admin\Desktop\3.jpg" alt="SKY">
                <div class="SKY">PLANTS</div>
            </div>
            <div class="image">
                <img src="c:\Users\admin\Desktop\4.jpg" alt="FLOWER">
                <div class="FLOWER">DARK SKY</div>
            </div>
            <div class="image">
                <img src="c:\Users\admin\Desktop\IMAGE 4.jpg" alt="SUNSET">
                <div class="SUNSET">SUNSET</div>
            </div>
        </div>
        <button id="nextBtn">❯</button>
    </div>

    <footer>
        Created by Taranikka A | Reg No: 212223220115
    </footer>

    <script src="script.js"></script>
</body>
</html>

```
### style.css:
```

body {
    font-family: Arial, sans-serif;
    text-align: center;
    background: #f4f4f4;
    margin: 0;
    padding: 0;
}


.gallery-container {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 20px auto;
    max-width: 600px;
    overflow: hidden;
}

.gallery {
    display: flex;
    transition: transform 0.5s ease-in-out;
}

.image {
    position: relative;
    margin: 5px;
}

.image img {
    width: 200px;
    height: 150px;
    border-radius: 10px;
    transition: 0.3s;
}

.image:hover img {
    transform: scale(1.1);
}

.caption {
    position: absolute;
    bottom: 10px;
    width: 100%;
    background: rgba(0, 0, 0, 0.7);
    color: white;
    padding: 5px;
    font-size: 14px;
    opacity: 0;
    transition: 0.3s;
}

.image:hover .caption {
    opacity: 1;
}

button {
    background-color: #333;
    color: white;
    border: none;
    padding: 10px;
    cursor: pointer;
    font-size: 20px;
    border-radius: 5px;
}

button:hover {
    background-color: #555;
}

footer {
    background: #222;
    color: white;
    padding: 10px;
    position: fixed;
    width: 100%;
    bottom: 0;
}
```

### script.js:
```
const gallery = document.querySelector(".gallery");
const prevBtn = document.getElementById("prevBtn");
const nextBtn = document.getElementById("nextBtn");

let scrollAmount = 0;
const scrollStep = 210; // Adjusted for image width + margin

nextBtn.addEventListener("click", () => {
    if (scrollAmount < (5 - 3) * scrollStep) { // Adjusted for 5 images
        scrollAmount += scrollStep;
    }
    gallery.style.transform = translateX(-${scrollAmount}px);
});

prevBtn.addEventListener("click", () => {
    if (scrollAmount > 0) {
        scrollAmount -= scrollStep;
    }
    gallery.style.transform = translateX(-${scrollAmount}px);
});
```

### OUTPUT:
![Screenshot 2025-03-22 144230](https://github.com/user-attachments/assets/fde12413-7194-4d39-b269-31314d2dd6eb)




