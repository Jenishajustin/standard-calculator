# Design of a Standard Calculator

## AIM:

To design a web application for a standard calculator.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.
### Step 2:
Change settings.py file to allow request from all hosts.
### Step 3:
Use CSS for creating attractive colors.
### Step 4:
Write JavaScript program for implementing five different operations.
### Step 5:
Validate the HTML and CSS code.
### Step 6:
Publish the website in the given URL.

## PROGRAM :
 ```html
 calc.html
 <!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="/static/css/style.css">
    <title>Calculator</title>
</head>

<body>
    <div class="container">
        <h1>Calculator</h1>

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button>(</button></td>
                    <td><button>)</button></td>
                    <td><button>C</button></td>
                    <td><button>%</button></td>
                </tr>
                <tr>
                    <td><button>7</button></td>
                    <td><button>8</button></td>
                    <td><button>9</button></td>
                    <td><button>X</button></td>
                </tr>
                <tr>
                    <td><button>4</button></td>
                    <td><button>5</button></td>
                    <td><button>6</button></td>
                    <td><button>-</button></td>
                </tr>
                <tr>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>3</button></td>
                    <td><button>+</button></td>
                </tr>
                <tr>
                    <td><button>0</button></td>
                    <td><button>.</button></td>
                    <td><button>/</button></td>
                    <td><button>=</button></td>
                </tr>
            </table>
        </div>
    </div>

</body>
<script src="/static/js/index.js"></script>
</html>
```
index.js
```javascript

let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }

    })
}
```
style.css
```css
.container{
    text-align: center;
    margin-top:23px
}

table{
    margin: auto;
}

input{
    border-radius: 21px;
    border: 5px solid #070707;
    font-size:34px;
    height: 65px;
    width: 456px;
}

button{
    border-radius: 20px;
    font-size: 40px;
    background: #ffe600;
    width: 102px;
    height: 90px;
    margin: 6px;
}

.calculator{ 
    border: 4px solid #030303;
    background-color: #07defa;
    padding: 23px;
    border-radius: 53px;
    display: inline-block;
    
}

h1{
    font-size: 28px;
    font-family: 'Courier New', Courier, monospace;
}
```

## OUTPUT:
![calc](https://user-images.githubusercontent.com/119405070/214778207-d01b2dcf-843e-4a5a-bb74-7f48b30e2c2b.png)
<br>

![calc1](https://user-images.githubusercontent.com/119405070/214778268-6162085e-dcae-4ce6-a5e0-b6039c3c7dd0.png)
<br>

![calc2](https://user-images.githubusercontent.com/119405070/214778317-9141d09f-879b-4b23-984d-39381dd47d7d.png)
<br>

## HTML Validator:
![calcvalid](https://user-images.githubusercontent.com/119405070/214778367-c1b5c8a5-e4cc-406d-876a-4f2f9e0c3cfb.png)
<br>

## Result:
The program for designing a simple calculator using javascript is executed successfully.

