Create a dockerfile for a Node.js Express application that:
- Uses Nodejs 20
- copies source code
- installs dependecies
- Exposes port 3000
- starts the application




use this simple express application

``` 
const express = require("express");

const app = express();

app.get("/", (req, res) => {
  res.send("Hello, World!");
});

app.get("/health", (req, res) => {
  res.json({ status: "ok" });
});

const PORT = process.env.PORT || 3000;

if (require.main === module) {
  app.listen(PORT, () => {
    console.log(`Server running on port ${PORT}`);
  });
}

module.exports = app;

```
