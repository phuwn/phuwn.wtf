---
title: Let’s Green Your GitHub
date: "2021-03-14T00:01:00.000Z"
template: "post"
draft: false
slug: "lets-green-your-github"
category: "Cool stuff"
tags:
  - "GitHub"
  - "Commit"
  - "Résume"
description: "Beautify your github to attract recruiters in a few steps"
socialImage: "/media/post_2_img_1.jpg"
---

![Beautiful Commit graph](/media/post_2_img_1.jpg)

Today we gonna talk about our contribution graph hehe. GitHub profile really does matter right? It stores all your works, your contributions, your techy life. It truly is your IT home. And yeah stuff in your house does reflect who you are. The contribution graph is one of them, it can amaze recruiters and other developers how hard-working you are. So people usually want a nice and tidy GitHub with a fancy contribution graph, they come up with a lot of stuff just to keep them keen on committing like 100 days coding challenge, daily commit routine, … But you’re not into stuff like that. You are that kind of guy who is too busy to commit daily or your company, your team simply doesn’t use GitHub as a main work resource manager. Or even worst, you are likely to push a giant commit that holds the whole feature than a teeny tiny commit but still want a green graph. Then, this article is perfect for you. Let’s plant some commits to green your GitHub forest.

### 1. Automatically A Commit A Day

Ok, so you want less cheating but still manage to commit every day? A simple script and Heroku will serve your purpose.

First, create a private repo to store your commits.

![Create a private repo on GitHub](/media/post_2_img_2.png)

Remember to change your contribution setting (in the Overview tab) to Private contributions to show your private commit and cheat commit without being detected.

![Change Contribution setting](/media/post_2_img_3.png)

Now, create a Heroku app.

![Create a Heroku app](/media/post_2_img_4.png)

Go to your terminal, clone my script repo [github.com/phuwn/a-commit-a-day](https://github.com/phuwn/a-commit-a-day). And in my repository, log in to your Heroku account and set up your app configuration like below.

```sh
# Go to your terminal, clone this repo
git clone https://github.com/phuwn/a-commit-a-day.git
cd a-commit-a-day

# Connect to Heroku and setup your app
heroku login
heroku git:remote -a a-commit-a-day

# Set buildpack for our app, since my script are shell script, so...
heroku buildpacks:set https://github.com/niteoweb/heroku-buildpack-shell.git

# Provide your GitHub details
# Your commit repo url
heroku config:set GITHUB_CLONE_URL=https://{YOUR_GITHUB_ACCESS_TOKEN}@{YOUR_GITHUB_REPO}
heroku config:set GITHUB_USER_EMAIL={YOUR_GITHUB_EMAIL}
heroku config:set GITHUB_USER_NAME={YOUR_GITHUB_NAME}

# Push my script to your app
git push heroku main
```

Check your config at Setting > Config Vars

![Check Heroku app setting](/media/post_2_img_5.png)

To set up a scheduler that commits for you daily.

- Set your credit card information in Heroku at [Manage Account > Billing](https://dashboard.heroku.com/account/billing)

![Set credit card info](/media/post_2_img_6.png)

- On Terminal, go to my repository and install add-on Scheduler with heroku addons:create scheduler:standard

- Set up the Schedule Job

![Go to Schedule Panel](/media/post_2_img_7.png)

![Set up the Schedule Job](/media/post_2_img_8.png)

- Check your app status with heroku log --tails

And now you’ll have A commit a day.

### 2. Spray your Contribution Graph with GitHub Spray

![Spray Example](/media/post_2_img_9.jpeg)

[Annihil/github-spray](https://github.com/Annihil/github-spray) is a CLI tool written in NodeJS that could help you transform your contribution graph into some fancy artwork.

All you need to do is

- Install the tool npm i -g github-spray

- Design your message. Ex:github-spray -t "Hello World"

- You can even draw out your own message using the [Spray Generator](https://annihil.github.io/github-spray-generator/)

![Draw and generate message](/media/post_2_gif_1.gif)

![My own repo spray](/media/post_2_img_10.png)

So cool right? Try them out and show me your new GitHub graph hehe.

### Reference

- [3 Step Setting up Heroku schedule (cron) job](https://hackernoon.com/3-step-setting-up-heroku-schedule-cron-job-example-tutorial-set-up-node-dyno-14d1d8ccfe4f)

- [👾 Hack Your GitHub Contribution Graph ░▒▓█](https://hackernoon.com/hack-your-github-contribution-graph-d88bdb417351)

- [Annihil/github-spray](https://github.com/Annihil/github-spray)

- [Making Your Github Green Again](https://medium.com/@olyaB/making-your-github-green-again-dab6f414b04b)

---

[My post on Medium](https://phuwn.medium.com/lets-green-your-github-e7618122dc2). Would you care for giving me a clap? Thank you :D
