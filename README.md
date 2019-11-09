
## HOMEWORK 3: Password Generator



## Description
Create an application that generates a random password based on user-selected criteria. This app will run in the browser and feature dynamically updated HTML and CSS powered by your JavaScript code.
The user will be prompted to choose from the following password criteria:


Length (must be between 8 and 128 characters)


Character type:


Special characters (see examples)


Numeric characters


Lowercase characters


Uppercase characters




The application should validate user input and ensure that at least one character type is selected.
Once all prompts are answered, the user will be presented with a password matching the answered prompts. Displaying the generated password in an alert is acceptable, but attempt to write the password to the page instead.
As a bonus, the user should also have the option to click a button to copy the password to their clipboard.
Your application should have a clean and polished user interface and be responsive, ensuring that it adapts to multiple screen sizes.
Your application should be deployed to GitHub Pages.
Your application's GitHub repository should contain a README.md file explaining the purpose and functionality of the application. The README.md file should include a screenshot of the completed application as well as a link to the deployed GitHub Pages URL.
https://vanderbilt.bootcampcontent.com/vanderbilt_coding_bootcamp/VU-NSH-FSF-PT-10-2019-U-C/raw/master/03-JavaScript/02-Homework/Assets/03-JavaScript-homework-demo.png

## User Story
AS AN employee with access to sensitive data
I WANT to randomly generate a password that meets certain criteria
SO THAT I can create a strong password that provides greater security

## Business Context
For companies that handle large amounts of sensitive data, weak passwords can pose a real security threat. An application that can generate strong passwords quickly and effortlessly saves employees time and ensures secure access to data.

## Acceptance Criteria
GIVEN that a user needs a new, secure password
WHEN prompted for password criteria
THEN a password is generated


## Commit Early and Often
One of the most important skills to master as a web developer is version control. Building the habit of committing via Git is important for two reasons:


## Your commit history is a signal to employers that you are actively working on projects and learning new skills.


## Your commit history allows you to revert your codebase in the event that you need to return to a previous state.


## Follow these guidelines for committing:


## Make single-purpose commits for related changes to ensure a clean, manageable history. If you are fixing two issues, make two commits.


## Write descriptive, meaningful commit messages so that you and anyone else looking at your repository can easily understand its history.


## Don't commit half-done work, for the sake of your collaborators (and your future self!).


## Test your application before you commit to ensure functionality at every step in the development process.


## We would like you to have well over 200 commits by graduation, so commit early and often!

## Submission on BCS
You are required to submit the following:


The URL of the deployed application


The URL of the GitHub repository



## © 2019 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.


## HTML 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <script src="C:\Users\User\Desktop\workspace\HW3-Password-Generator\HW3.jsx"></script>
    <link rel="stylesheet" href="C:\Users\User\Desktop\workspace\HW3-Password-Generator\style.css">
</head>
<body>
    <form name="myform" method="post" action="">
        <input type="hidden" name="length" value="10">
        <table width="100%" border="0"></table>

    <div class="all"> 
        <center>
            <div class="container">
                <center>
              <div class="box1">Password Generator</div>
              <br>
              <br>
              <br>
                <div class="password">Generate a Password</div>
                <td>
                    <input name="row_password" type="text" size="100">&nbsp;
                    <br>
                    <input type="button" class="button" value="Generate Password" onClick="generate();" tabindex="2">
                    <input type="button" class="copy" value="Copy to Clipboard" onClick="copy();" tabindex="2">
                </center>          
                
        </center
                
    </div>
    </table>
    </form>
</body>
</html>

## CSS
.all {
    background-color: lightblue;
    width: fit-content
    padding: 25px;
   

}




.box1 {
    font: bold;
    font-size: 32px;
    background-color: lightgray;
    width: fit-content;
     margin: 0;
    height: fit-content;
    padding: 5px;
    ;
}

input {
  widows: 100px; height: 100px; border: 1px solid #999999; padding: 5px; 
}

.password {
    font: bold;
    font-size: 32px;
}

.button {
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
    color: white;
    background-color: red;
    width: fit-content;
    
    
    
}

.button2 {
    font-size: 32px;
    font-family: Arial, Helvetica, sans-serif;
    color: red;
       
}

.copy {
    font-size: 18px;
    font-family: Arial, Helvetica, sans-serif;
    color: white;
    background-color: lightgray
    width: fit-content;  
}


## JAVASCRIPT 
function randomPassword(length) {
    var chars = "abcdefghijklmnopqrstuvwxyz!@#$%^&*()-+<>ABCDEFGHIJKLMNOP1234567890";
    var pass = "";
    for (var x = 0; x < length; x++) {
        var i = Math.floor(Math.random() * chars.length);
        pass += chars.charAt(i);
    }
    return pass;
}

function generate() {
    myform.row_password.value = randomPassword(myform.length.value);
}

function copyToClipboard(text) {
    window.prompt("Copy to clipboard: Ctrl+C, Enter", text);
}s
