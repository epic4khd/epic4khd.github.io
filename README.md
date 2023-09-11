<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome Website</title>
    <style>
        body {
            background-color: white;
            text-align: center;
            font-size: 24px;
            padding: 20px;
        }
        button {
            padding: 10px 20px;
            font-size: 18px;
            cursor: pointer;
            border-radius: 10px; /* Rounded corners added */
        }
    </style>
</head>
<body>
    <div id="page1">
        <h1>Announcements</h1>
        <button onclick="showPage(2)">Go To The Chatroom</button>
    </div>

    <div id="page2" style="display: none;">
        <h1>Welcome to Page 2</h1>
        <button onclick="showPage(1)">Go to Page 1</button>
    </div>

    <script>
        function showPage(pageNumber) {
            if (pageNumber === 1) {
                document.getElementById('page1').style.display = 'block';
                document.getElementById('page2').style.display = 'none';
            } else if (pageNumber === 2) {
                document.getElementById('page1').style.display = 'none';
                document.getElementById('page2').style.display = 'block';
            }
        }
    </script>
</body>
</html>
