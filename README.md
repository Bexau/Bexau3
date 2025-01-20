<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ChatGPT-like Assistant</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div id="app">
        <header>
            <h1>AI Assistant</h1>
            <p>Ask anything and get an answer.</p>
        </header>

        <section id="chatbox">
            <div id="messages"></div>
            <input type="text" id="userInput" placeholder="Type your query here..." onkeydown="if(event.key === 'Enter'){sendMessage();}">
            <button onclick="sendMessage()">Send</button>
        </section>
    </div>

    <script src="app.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: black;
    color: white;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
}

header {
    text-align: center;
    margin-bottom: 30px;
}

#chatbox {
    width: 80%;
    max-width: 600px;
    background-color: #333;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}

#messages {
    max-height: 300px;
    overflow-y: scroll;
    margin-bottom: 10px;
    color: lightgray;
}

#userInput {
    width: 80%;
    padding: 10px;
    background-color: #555;
    border: none;
    color: white;
    border-radius: 5px;
    margin-right: 10px;
}

button {
    padding: 10px 20px;
    background-color: #008CBA;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #005f73;
}
// This function will send the message and display a mock response.
function sendMessage() {
    const userInput = document.getElementById("userInput").value;
    const messagesDiv = document.getElementById("messages");

    if (userInput.trim() === "") {
        alert("Please type something before sending.");
        return;
    }

    // Display user message
    const userMessageDiv = document.createElement("div");
    userMessageDiv.textContent = `You: ${userInput}`;
    messagesDiv.appendChild(userMessageDiv);

    // Clear input field
    document.getElementById("userInput").value = "";

    // Display loading message
    const loadingMessageDiv = document.createElement("div");
    loadingMessageDiv.textContent = "AI is typing...";
    messagesDiv.appendChild(loadingMessageDiv);

    // Simulate AI response (this is where you'd hook into a real API)
    setTimeout(() => {
        loadingMessageDiv.textContent = "AI: Here's a response to your question.";
        messagesDiv.scrollTop = messagesDiv.scrollHeight;
    }, 1500);  // Simulate 1.5s delay for AI response
}
git clone https://github.com/your-username/chatgpt-like-assistant.git
git add .
git commit -m "Initial commit"
git push origin main
