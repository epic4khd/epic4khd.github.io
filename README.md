<!DOCTYPE html>
<html>
<head>
    <title>HTML Code Runner</title>
</head>
<body>
    <h1>HTML Code Runner</h1>
    
    <p>Paste your HTML code below:</p>
    
    <textarea id="htmlCode" rows="10" cols="50"></textarea>
    
    <br>
    
    <button onclick="runCode()">Run Code</button>
    
    <hr>
    
    <h2>Output:</h2>
    
    <iframe id="output" width="100%" height="400"></iframe>

    <script>
        function runCode() {
            const htmlCode = document.getElementById("htmlCode").value;
            const outputFrame = document.getElementById("output");
            
            // Clear the existing content in the output frame
            outputFrame.contentDocument.body.innerHTML = '';
            
            // Write the user's HTML code to the output frame
            outputFrame.contentDocument.open();
            outputFrame.contentDocument.write(htmlCode);
            outputFrame.contentDocument.close();
        }
    </script>
</body>
</html>
