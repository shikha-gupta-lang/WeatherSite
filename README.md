# WeatherSite

🌦 Weather Site (Full Stack)
A full-stack weather application that allows users to search for real-time weather information for any city using OpenWeather API.
It includes:

Frontend: Beautiful animated UI with weather search and confetti animations.

Backend: Node.js + Express server, proxying API requests securely using environment variables.

📁 Project Structure
pgsql
Copy
Edit
weather-site/
│
├── frontend/
│   ├── index.html
│   ├── styles.css
│   ├── script.js
│
├── weather-backend/
│   ├── server.js
│   ├── routes/
│   │   └── weather.js
│   ├── .env
│   ├── package.json
│   └── node_modules/  (generated after npm install)
│
└── README.md
🚀 Live Demo
https://weather-site-5gf8.onrender.com

🧑‍💻 Technologies Used
Frontend: HTML, CSS, JavaScript, GSAP Animation

Backend: Node.js, Express, Axios, dotenv

API: OpenWeather API

⚙️ Backend Setup
1️⃣ Clone the repository
bash
Copy
Edit
git clone https://github.com/your-username/weather-site.git
cd weather-site/weather-backend
2️⃣ Install dependencies
bash
Copy
Edit
npm install
3️⃣ Create .env file
In the weather-backend/ folder create a file called .env:

ini
Copy
Edit
PORT=5000
OPENWEATHER_API_KEY=your_openweather_api_key
🔑 Replace your_openweather_api_key with your actual API key from OpenWeather.

4️⃣ Start the server locally
bash
Copy
Edit
node server.js
Your backend will run on:

arduino
Copy
Edit
http://localhost:5000
⚙️ Frontend Setup
Open the index.html file from frontend/ folder directly in your browser for local testing.

👉 Make sure your script.js has correct API URL pointing to your backend:

javascript
Copy
Edit
const apiUrl = "http://localhost:5000/api/weather?units=";
🌐 Deployment on Render
Backend
Build Command:

nginx
Copy
Edit
npm install
Start Command:

nginx
Copy
Edit
node server.js
Environment Variables on Render:

OPENWEATHER_API_KEY = your_openweather_api_key

PORT = 10000 (Render automatically assigns PORT if not manually set, use environment variable PORT in your server.js)

⚠ In server.js you already have:

javascript
Copy
Edit
const PORT = process.env.PORT || 5000;
So you're ready for Render!

Frontend
You can deploy frontend separately on Netlify, Vercel or GitHub Pages.

Update API URL in frontend script.js to point to your Render backend deployment:

javascript
Copy
Edit
const apiUrl = "https://your-backend-url.onrender.com/api/weather?units=";
💡 Future Improvements
Add 5-day forecast

User location auto-detect on load

Error handling improvements

UI polish

✨ Credits
OpenWeather API

GSAP Animations

Confetti effects
