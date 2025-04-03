const express = require("express");
const fetch = require("node-fetch");
const app = express();

app.use(express.json());

// Enable CORS to allow your frontend to call this backend
app.use((req, res, next) => {
  res.header("Access-Control-Allow-Origin", "*");
  res.header("Access-Control-Allow-Headers", "Origin, X-Requested-With, Content-Type, Accept");
  next();
});

app.post("/recipe", async (req, res) => {
  const { ingredients } = req.body;
  try {
    const response = await fetch("https://api.openai.com/v1/chat/completions", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
        "Authorization": `Bearer ${process.env.OPENAI_API_KEY}`
      },
      body: JSON.stringify({
        model: "gpt-3.5-turbo",
        messages: [
          {
            role: "user",
            content: `I have these ingredients: ${ingredients.join(", ")}. Suggest a Michelin star-level recipe using these ingredients. Include the recipe name, ingredients list, and short instructions.`
          }
        ],
        max_tokens: 150
      })
    });
    const data = await response.json();
    const recipe = data.choices[0].message.content;
    res.json({ recipe });
  } catch (error) {
    res.status(500).json({ error: "Failed to fetch recipe" });
  }
});

const port = process.env.PORT || 3000;
app.listen(port, () => console.log(`Server running on port ${port}`));
