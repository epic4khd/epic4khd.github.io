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
            border-radius: 10px;
        }
        /* Change background color for both pages */
        #page1, #page2 {
            background-color: rgb(98, 19, 135);
            color: white; /* Set text color to contrast with the background */
            padding: 20px;
        }
    </style>
</head>
<body>
    <div id="page1">
        <h1>Announcements</h1>
        <!-- Added image with rounded corners -->
        <img src="https://o.remove.bg/downloads/fd9914c7-05cf-48da-808f-694af04dd804/Epic__Logo-removebg-preview.png" alt="Image" style="border-radius: 10px; max-width: 100%; height: auto;">
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
