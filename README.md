# Web Scraping Price API
## Description
This project creates a RESTful API that scrapes a webpage and returns the price of a product. It is built using Node.js, Express, Axios, and Cheerio.

- Motivation: The API allows users to easily access the latest price of a product from a specific webpage.
- Problem solved: Users can now access the latest price without manually visiting the webpage and searching for the price.
- Learning: This project demonstrates the use of web scraping techniques, RESTful API creation, and deployment on Heroku.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Deployment](#deployment)
- [Credits](#credits)
- [License](#license)

## Installation
To set up the project locally, follow these steps:

1. Clone the repository: `git clone https://github.com/your-username/your-repo-name.git`
2. Change to the project directory: `cd your-repo-name`
3. Install dependencies: `npm install`

## Usage
To run the project locally:

1. Start the server: `node app.js`
2. Access the API: `http://localhost:3000/price`

## Deployment
To deploy the API on Heroku:

1. Install the [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)
2. Log in to your Heroku account: `heroku login`
3. Create a new app: `heroku create your-app-name`
4. Add a Procfile with the following content: `web: node app.js`
5. Commit your changes to a Git repository and push the code to Heroku:
