# Bexau3
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AI Assistant</title>
  <link rel="stylesheet" href="styles.css">
  <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>
</head>
<body>

  <div id="app">
    <header>
      <h1>AI Assistant</h1>
      <p>Your friendly AI assistant</p>
    </header>

    <section id="chatbox">
      <div id="messages"></div>
      <input type="text" id="userInput" placeholder="Ask me something..." />
      <button onclick="sendMessage()">Send</button>
    </section>

    <section id="assistant-settings">
      <h3>Settings</h3>
      <label for="tone">Choose Tone:</label>
      <select id="tone">
        <option value="friendly">Friendly</option>
        <option value="formal">Formal</option>
        <option value="technical">Technical</option>
      </select>
    </section>
  </div>

  <script src="app.js"></script>
</body>
</html>
