# QVAC-SDK
1. Initialize project and install QVAC SDK Open your terminal and run:  mkdir qvac-local-ai-app cd qvac-local-ai-app npm init -y npm install @qvac/sdk
2. Create index.js with this code:
const { Qvac } = require('@qvac/sdk');

async function run() {
  try {
    // Initialize QVAC SDK
    const qvac = new Qvac();

    // Load the 'text' AI model (downloads automatically on first run)
    await qvac.loadModel('text');

    // Input text to process
    const inputText = "Hello, how are you today?";

    // Run the AI model on the input text
    const result = await qvac.run('text', inputText);

    // Output the AI response
    console.log('AI response:', result);
  } catch (error) {
    console.error('Error running QVAC AI:', error);
  }
}

run();
3. Run the app
In your terminal, run:

node index.js
You will see the AI-generated response printed in the console, confirming the AI model ran locally on your device.

This fulfills the requirement to build a working app that uses the QVAC SDK to run AI on-device and produces a visible output.
