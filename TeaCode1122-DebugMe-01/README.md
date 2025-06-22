🐞 Debug Me #1: Docker Port Not Working

📌 Scenario

You built and ran a Node.js app in Docker using:

docker run -d myapp

But when you go to http://localhost:3000, it doesn't work. No errors in logs. Blank browser.


---

❓ What Went Wrong?

You didn’t expose the container’s port to your host. So Docker is running the app, but your browser can't access it.


---

🌟 Submit Your Fix

Share your output in the group

Bonus points for adding logs or screenshots

Top solvers get featured every Saturday 🎉
