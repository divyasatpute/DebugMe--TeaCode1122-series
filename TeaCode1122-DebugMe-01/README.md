🐞 Debug Me #1: Docker Port Not Working

📌 Scenario

You built and ran a Node.js app in Docker using:

docker run -d myapp

But when you go to http://localhost:3000, it doesn't work. No errors in logs. Blank browser.


---

❓ What Went Wrong?

You didn’t expose the container’s port to your host. So Docker is running the app, but your browser can't access it.


---

✅ Solution

Use the -p flag to map ports:

docker run -d -p 3000:3000 myapp

3000:3000 means: Host port 3000 ➝ Container port 3000



---

🛠️ Dockerfile Example (for reference)

FROM node:18-alpine
WORKDIR /app
COPY . .
RUN npm install
EXPOSE 3000
CMD ["node", "app.js"]


---

🧠 What You Learn:

Why Docker ports must be explicitly mapped

Importance of EXPOSE and -p when running containers



---

🔁 How to Reproduce

git clone https://github.com/<your-user>/TeaCode1122-DebugMe-Series
cd DebugMe-01-Docker-Port
npm install
docker build -t debugme1 .
docker run -p 3000:3000 debugme1

Visit: http://localhost:3000


---

🌟 Submit Your Fix

Share your output in the group

Bonus points for adding logs or screenshots

Top solvers get featured every Saturday 🎉
