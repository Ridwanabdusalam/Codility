# Project Setup Guide

## Overview
This project is designed to automatically update a text file in the repository by appending a new line to it. The update process is controlled by GitHub Actions, which are configured to run at specific times throughout the day.

## Repository Structure
- `hello_world.txt`: A dummy file that gets updated with an extra line each time the GitHub Actions workflow runs.
- `.github/workflows/scheduler.yml`: The GitHub Actions workflow configuration file. This is set up to run the code randomly up to 8 times per day, with a 33% chance of running each time.

## Setup Instructions

### Step 1: Create a Private GitHub Repository
1. If you don’t already have one, create a new **private** GitHub repository. This is where you’ll implement the automated file updates. To do this, go to https://github.com/dashboard and click on **New**. Enter a **Repository** name, and select **Private** and lastly, **Create Repository**.

### Step 2: Prepare the Files
0. Download my repository here: https://github.com//ridwanabdsalam/Daily-Updates/archive/refs/heads/main.zip.
1. Locate `hello_world.txt` and `scheduler.yml` in your downloaded folder.
2. Place `hello_world.txt` in the main folder of your GitHub repository by drag and drop.
3. Open `scheduler.yml` in a text editor and copy paste its contents into `.github/workflows/` directory of your repository. To do this, go to your github and "Add file" > "Create new file". Then, name your file `.github/workflows/scheduler.yml` and paste the contents of the file here.
4. Make sure your `user.email` and `user.name` are correct at the end of the `scheduler.yml` and you are not using mine.

### Step 3: Generate a Personal Access Token
1. Navigate to your GitHub profile settings.
2. Go to Settings > Developer Settings > Personal Access Tokens > Tokens (Classic).
3. Click "Generate a New Token (Classic)".
4. Set the note to "My Private Project" and choose "No Expiration".
5. Select all checkboxes under Scopes for full permissions.
6. Click "Generate Token" and copy the generated token.

### Step 4: Add the Token to Your Repository
1. Go to your GitHub repository and click on Settings.
2. Navigate to Secrets and Variables > Actions.
3. Click "New repository secret".
4. Name the secret `PERSONAL_ACCESS_TOKEN`.
5. Paste the Personal Access Token you copied earlier into the Secret box.

## Running the Workflow
With these steps completed, your GitHub Actions workflow is set up to run every hour from 9 AM to 5 PM PST. This schedule ensures a constant update to your repository, helping to maintain an active GitHub timeline.

Enjoy your automated GitHub updates!
