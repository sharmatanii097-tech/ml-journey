# My ML Journey Setup

## Important Paths
- My ml-journey folder: C:\Users\deepa\OneDrive\Desktop\ml-journey
- Python version: 3.14.2
- GitHub username: [sharmatanii097-tech]

## To open my project in CMD always type:
cd C:\Users\deepa\OneDrive\Desktop\ml-journey

## Libraries installed:
- numpy
- pandas
- matplotlib
- scikit-learn
- jupyter

What is Git?
Think of Git like a save system in a video game.
In games you save your progress so if you die you can go back to your last save point.
Git does the same for your code:

You write code
You save it with Git
If you break something later — you go back to the last save
Every save is called a commit


What is GitHub?
If Git is your save system — GitHub is the cloud where those saves are stored online.

Git = saves on your computer
GitHub = saves on the internet

So even if your laptop breaks — your code is safe on GitHub forever.

Now Why These Two Commands
git init
git init
This means — "start tracking this folder with Git"
Like telling Git:

"Hey, watch this ml-journey folder. From now on track every change I make here."

Without this — Git doesn't know your folder exists.

git remote add origin
git remote add origin https://github.com/YOURUSERNAME/ml-journey.git
This means — "connect my local folder to my GitHub repository online"

remote = the online version on GitHub
origin = nickname for that online location
The URL = exact address of your GitHub repository

Think of it like:

"My folder on this laptop is connected to THIS specific place on GitHub. When I push code — send it there."


The Full Flow — How You Will Use This Every Day
Write code today
      ↓
git add .         (select all files to save)
      ↓
git commit -m "Day 1 - NumPy basics"    (save with a message)
      ↓
git push          (send to GitHub online)




## How to Switch GitHub Accounts in CMD

Step 1: cmdkey /delete:git:https://github.com
Step 2: git push
Step 3: Login with whichever account needed

My ML account: sharmatanii097-tech
My other account: tanishashr99-new

Note: No accounts get deleted. Just switching login.



## How to Open Jupyter Anytime

Step 1: Open CMD
Step 2: cd C:\Users\deepa\OneDrive\Desktop\ml-journey
Step 3: python -m notebook
Step 4: Browser opens automatically
Step 5: Keep CMD minimized - never close it!

Note: localhost:8888 = running on MY computer, not internet