# INTRODUCTION:
Built on Chrome's V8 JavaScript engine, Node.js compiles code into native machine code, making it highly efficient. backend programming language.

Developers can use JavaScript on both the client and server side, streamlining the development process.

# HOW PROJECT WORKS:
For the sake of this project , we are generating a QR code using the backend framework Node.JS. In order to make this project work, we need to download the packages require to execute the code. These packages include 'inquirer' & 'qr-image' that can be downloaded from NPM website. [NPM Link](https://www.npmjs.com/)

To install packages we use command;

    - npm install inquirer qr-image

# SYNTAX FOR INQUIRER:

    - import inquirer from 'inquirer';

     inquirer
     .prompt([
     /* Pass your questions in here */
     ])
    .then((answers) => {
    // Use user feedback for... whatever!!
    })
    .catch((error) => {
    if (error.isTtyError) {
    // Prompt couldn't be rendered in the current environment
    } else {
    // Something else went wrong
    }
    });
1- The import command imports the "inquirer" module, a popular package for handling command-line user prompts.

2- .prompt([...]) is a method that takes an array of question objects and returns a promise.
Each object in the array defines a question and its properties (such as type, name, message, choices, etc.).

3- The .then((answers) => { ... }) block runs once the user has answered all prompts.

4- The .catch((error) => { ... }) block handles any errors that might occur during execution.

# SYNTAX FOR QR-IMAGE:

  
    -  import qr from 'qr-image';
    
    var qr_svg = qr.image('I love QR!', { type: 'svg' });
    
    qr_svg.pipe(require('fs').createWriteStream('i_love_qr.svg'));

  1- This imports the qr-image package.The qr-image module is used to generate QR codes in formats like PNG, SVG, PDF, and EPS.

  2- qr.image() is a function from the qr-image package that generates a QR code.

  3- The first argument 'I love QR!' is the content that will be encoded in the QR code.The second argument { type: 'svg' } specifies the output format of the QR code.

  4- .pipe(require('fs').createWriteStream()); writes the stream (i_love_qr.svg) into a file.


# CONCLUSION: 🚀🚀🚀

By using the above two packages, one can easily generate a QR code for their desired website. We just need to provide the URL for the website in the prompt and it wil generate a QR code and the text file in the backend. 
