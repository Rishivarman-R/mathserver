# Ex.05 Design a Website for Server Side Processing
# Date:30/11/2024
# AIM:
To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side.

# FORMULA:
P = I2R
P --> Power (in watts)
 I --> Intensity
 R --> Resistance

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Create python programs for views and urls to perform server side processing.

## Step 5:
Create a HTML file to implement form based input and output.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Power of a lamp</title>
    <style>
        body {
            background-color: rgb(171, 159, 153);
            font-family: 'Lora', serif;
        }
        .container {
            width: 400px;
            margin: 50px auto;
            text-align: center;
            background-color: rgb(35, 244, 212);
            color: rgb(33, 19, 222);
            padding: 20px;
            border: 3px dashed rgb(3, 16, 19);
            border-radius: 10px;
        }
        input[type="text"] {
            width: 80%;
            padding: 5px;
            margin: 10px 0;
        }
        input[type="submit"] {
            padding: 5px 10px;
            background-color: rgb(193, 2, 72);
            color: rgb(3, 246, 145);
            border: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="container">
    <h1>Power of a lamp</h1>

    <form method="POST">
        {% csrf_token %}
        <label for="intensity">Intensity (I in Amps):</label>
        <input type="text" name="intensity" id="intensity" required><br><br>

        <label for="resistance">Resistance (R in Ohms):</label>
        <input type="text" name="resistance" id="resistance" required><br><br>
        <font ="red">
        <button type="submit"><b>calculate</b></button>
    </font>
    </form>

    {% if power is not None %}
        <h2>Calculated Power: {{ power }} Watts</h2>
    {% endif %}
</div>
</body>
</html>


```
# SERVER SIDE PROCESSING:
![Screenshot (39)](https://github.com/user-attachments/assets/e278b2b7-2a96-4bf0-be86-656f1f3c24f3)


# HOMEPAGE:

![Screenshot (40)](https://github.com/user-attachments/assets/97c91851-4b27-4b3f-afc6-3ecc90db39bf)

# RESULT:
The program for performing server side processing is completed successfully.
