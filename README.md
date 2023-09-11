<div id="page2" style="display: none;">
    <h1>Welcome to the Chatroom</h1>
    <div id="chat-container">
        <div id="chat-messages"></div>
        <input type="text" id="message-input" placeholder="Type your message...">
        <button onclick="sendMessage()">Send</button>
    </div>
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

    function sendMessage() {
        var message = document.getElementById('message-input').value;
        if (message.trim() !== '') {
            var chatMessages = document.getElementById('chat-messages');
            var newMessage = document.createElement('div');
            newMessage.textContent = message;
            chatMessages.appendChild(newMessage);
            document.getElementById('message-input').value = '';
        }
    }
</script>
