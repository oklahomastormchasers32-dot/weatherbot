<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Weather Bot</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 10px; }
    #chatbox { border: 1px solid #ccc; padding: 10px; width: 300px; height: 400px; overflow-y: auto; }
    #userInput { width: 240px; }
  </style>
</head>
<body>
  <h2>Weather Bot</h2>
  <div id="chatbox"></div>
  <input type="text" id="userInput" placeholder="Ask me about Tulsa weather" />
  <button onclick="sendMessage()">Send</button>

  <script>
    const chatbox = document.getElementById('chatbox');
    const userInput = document.getElementById('userInput');

    function appendMessage(sender, text) {
      const msg = document.createElement('div');
      msg.textContent = `${sender}: ${text}`;
      msg.style.margin = '8px 0';
      msg.style.fontWeight = sender === 'Bot' ? 'bold' : 'normal';
      chatbox.appendChild(msg);
      chatbox.scrollTop = chatbox.scrollHeight;
    }

    function sendMessage() {
      const userText = userInput.value.trim();
      if (!userText) return;
      appendMessage('You', userText);
      userInput.value = '';

      // Simple weather response logic (replace with real API calls later)
      let botResponse = 'Sorry, I can only talk about Tulsa weather right now.';
      if (userText.toLowerCase().includes('temperature')) {
        botResponse = 'The current temperature in Tulsa is 85°F.';
      } else if (userText.toLowerCase().includes('humidity')) {
        botResponse = 'Humidity in Tulsa is about 65%.';
      } else if (userText.toLowerCase().includes('dew point')) {
        botResponse = 'The dew point in Tulsa is around 62°F.';
      } else if (userText.toLowerCase().includes('wind')) {
        botResponse = 'Winds are currently 10 mph from the south.';
      } else if (userText.toLowerCase().includes('hi') || userText.toLowerCase().includes('hello')) {
        botResponse = 'Hello! I am your Tulsa weather bot.';
      }

      setTimeout(() => appendMessage('Bot', botResponse), 500);
    }
  </script>
</body>
</html>
