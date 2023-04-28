# Web Scraping Price API
## To create a RESTful API that scrapes the given website and returns the price, I recommend using Node.js with the Express framework and the cheerio library for web scraping.

 

    Create a Node.js project: Initialize a new Node.js project by running npm init in your terminal. Install the required dependencies by running npm install express cheerio axios.

    Create the API using Express: Create a new file, app.js, and set up an Express server with a single route for the /price endpoint. Use the axios library to make HTTP requests and cheerio for web scraping. Here's a sample code snippet:

const express = require('express');
const axios = require('axios');
const cheerio = require('cheerio');

const app = express();

app.get('/price', async (req, res) => {
  try {
    const response = await axios.get('https://www.metal.com/Lithium-ion-Battery/202303240001');
    const $ = cheerio.load(response.data);
    const price = $('.detail___2oeiJ .left___wCEQV .strong___1JlBD').text();

    res.json({ price });
  } catch (error) {
    res.status(500).json({ message: 'An error occurred while fetching the price.' });
  }
});

const PORT = process.env.PORT || 3000;
app.listen(PORT, () => console.log(`Server running on port \${PORT}`));


Handle errors: In the code snippet above, we use a try-catch block to handle errors during the HTTP request and web scraping. If an error occurs, the API will return a 500 status code with a descriptive error message.
