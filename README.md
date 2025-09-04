WanderLog is a web application that lets you keep track of all the countries you’ve visited. The app highlights visited countries on a world map and keeps a running total of your travel progress.

Built with Node.js, Express, PostgreSQL, and EJS, it’s a full-stack project to practice database integration, server-side rendering, and interactive front-end features.

------------------
🚀 Features

✅ Add new countries by name (validated against a master country list).

✅ Highlights visited countries on an interactive SVG world map.

✅ Displays a live counter of total visited countries.

✅ Error handling for duplicates and invalid country names.

✅ Responsive front-end with EJS templates and CSS.

---------------------
🛠️ Tech Stack

Backend: Node.js, Express.js

Database: PostgreSQL

Frontend: EJS, HTML5, CSS3, Vanilla JavaScript

Other: Body-parser, pg (node-postgres)

-----------------------------

📂 Project Structure

📦 WanderLog
 ┣ 📂 public          # Static assets (CSS, images, etc.)
 ┣ 📂 views           # EJS templates (index.ejs)
 ┣ 📜 index.js        # Main server file
 ┣ 📜 package.json    # Dependencies and scripts
 ┣ 📜 README.md       # Project documentation

------------------------------------
🗄️ Database Setup

Two tables are used:

1. countries (Master list of countries)
CREATE TABLE countries(
id SERIAL PRIMARY KEY,
country_code CHAR(2),
country_name VARCHAR(100)
);

2. visited_countries (User’s visited countries)
id	SERIAL PRIMARY KEY Unique identifier
country_code	CHAR(2)	References countries.country_code

