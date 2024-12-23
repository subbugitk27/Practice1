// server.js
const express = require('express');
const app = express();
const port = 3000;

// Serve static files (optional if you have assets like images or stylesheets)
app.use(express.static('public'));

// Define the route to serve the HTML content
app.get('/', (req, res) => {
  res.send(`
    <!DOCTYPE html>
    <html>
    <head>
      <meta charset="utf-8">
      <title>Sample Deployment</title>
      <style>
        body {
          color: #ffffff;
          background-color: #0188cc;
          font-family: Arial, sans-serif;
          font-size: 14px;
        }

        h1 {
          font-size: 500%;
          font-weight: normal;
          margin-bottom: 0;
        }

        h2 {
          font-size: 200%;
          font-weight: normal;
          margin-bottom: 0;
        }
      </style>
    </head>
    <body>
      <div align="center">
        <h1>WELCOME TO NODE JS</h1>
        <h2>This is Node JS applciation</h2>
        <p>For next steps, read the <a href="http://aws.amazon.com/documentation/codedeploy" target="_blank">AWS CodeDeploy Documentation</a>.</p>
      </div>
    </body>
    </html>
  `);
});

// Start the server
app.listen(port, () => {
  console.log(`Server running at http://13.235.74.88:${port}`);
});