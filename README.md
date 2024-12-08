# Ex.08 Design of Interactive Image Gallery
# Date:20/11/2024
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
```python
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>image gallery</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
</head>

<style>

    body {
    margin: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    height: 100vh;
    background: black;
    overflow: hidden;
  }
  .image-container {
    position: relative;
    width: 200px;
    height: 200px;
    transform-style: preserve-3d;
    transform: perspective(1000px) rotateY(0deg);
    transition: transform 0.9s;
  }
  .image-container span {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    transform: rotateY(calc(var(--i) * 45deg)) translateZ(400px);
  }
  .image-container span img {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
  }
  .btn-container {
    position: relative;
    width: 80%;
  }
  .btn {
    position: absolute;
    bottom: -80px;
    background: crimson;
    color: #fff;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
  }
  #prev {
    left: 20%;
  }
  #next {
    right: 20%;
  }
  .btn:hover {
    filter: brightness(1);
  }

</style>

<body>

    <div class="image-container">

        <span style="--i:1">
            <img src="/static/img1.jpg" width="220" height="150">
        </span>

        <span style="--i:2">
            <img src="/static/img2.jpg" width="220" height="150">
        </span>

        <span style="--i:3">
            <img src="/static/img9.webp" width="220" height="150">
        </span>

        <span style="--i:4">
            <img src="/static/img11.jpg" width="220" height="150">
        </span>

        <span style="--i:5">
            <img src="/static/img5.jpg" width="220" height="150">
        </span>

        <span style="--i:6">
            <img src="/static/img6.jpg" width="220" height="150">
        </span>

        <span style="--i:7">
            <img src="/static/img7.jpg" width="220" height="150">
        </span>

        <span style="--i:8">
            <img src="/static/img8.jpg" width="220" height="150">
        </span>


    </div>

    <div class="btn-container">
        <button class="btn" id="prev">PREV</button>
        <button class="btn" id="next">NEXT</button>
    </div>

    <script>

      const imageContainer = document.querySelector('.image-container');
      const prevBtn = document.getElementById('prev');
      const nextBtn = document.getElementById('next');
      
      let x=0;
      prevBtn.addEventListener('click',( ) => {
          x=x+45
          rotate()
      })
      nextBtn.addEventListener('click',( ) => {
          x=x-45
          rotate()
      })
      function rotate() {
          imageContainer.style.transform=`perspective(1000px) rotateY(${x}deg)`;
      }
      
    </script>

</body>
</html>
```
# OUTPUT:
![Screenshot 2024-12-08 165122](https://github.com/user-attachments/assets/386954b1-544f-4562-a9e3-3ef456c188e2)


https://github.com/user-attachments/assets/7095b6a2-92e2-404e-a598-6986c92af41a



# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
