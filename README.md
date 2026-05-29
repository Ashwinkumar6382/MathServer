## AIM:
To create a web page to calculate total bill amount with GST from price and GST percentage using server-side scripts.

## FORMULA:
Bill = P + (P * GST / 100)
<br> P --> Price (in Rupees)
<br> GST --> GST (in Percentage)
<br> Bill --> Total Bill Amount (in Rupees)

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create a HTML file to implement form based input and output.

### Step 5:
Create python programs for views and urls to perform server side processing.

### Step 6:
Receive input values from the form using request.POST.get().

### Step 7:
Calculate the total bill amount (including GST).

### Step 8:
Display the calculated result in the server console.

### Step 9:
Render the result to the HTML template.

### Step 10:
Publish the website in Localhost.

## PROGRAM:
```
<html>
<head>
    <title>Power Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: lightgrey;
            margin: 20px;
            padding: 20px;
            text-align: center;
        }

        h1 {
            color: darkblue;
        }

        form {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 8px grey;
            display: inline-block;
            margin: auto;
        }

        label {
            font-weight: bold;
            color: black;
        }

        input[type="number"] {
            padding: 5px;
            margin: 10px 0;
            border: 1px solid black;
            border-radius: 4px;
        }

        button {
            background-color: darkblue;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: navy;
        }
    </style>
</head>
<body>
    <h1>Power Calculator</h1>
    <form method="POST">
        {% csrf_token %}
        <label for="I">Enter Current (I in Amps):</label>
        <input type="number" name="intensity" id="I" value="{{ I }}" required>
        <br><br>
        <label for="R">Enter Resistance (R in Ohms):</label>
        <input type="number" name="resistance" id="R" value="{{ R }}" required>
        <br><br>
        <button type="submit">Calculate Power</button>
        <br><br>
        <label for="power">Calculated Power (Watts):</label>
        <input type="number" name="power" id="power" value="{{ power }}" readonly>
    </form>
</body>
</html>
```

## OUTPUT - SERVER SIDE:
<img width="1049" height="651" alt="Screenshot 2026-05-26 094957" src="https://github.com/user-attachments/assets/3926bf5f-a250-4309-a810-a3d9bdc84d3e" />

## OUTPUT - WEBPAGE:
<img width="1049" height="651" alt="Screenshot 2026-05-26 094957" src="https://github.com/user-attachments/assets/683112da-a092-494b-bbe7-b7f061cc3004" />

## RESULT:
The a web page to calculate total bill amount with GST from price and GST percentage using server-side scripts is created successfully.
