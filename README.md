# Farm Scheduler

Farm Scheduler is a Python application that monitors Twitter for tweets containing a specified hashtag. When a tweet with the targeted hashtag is detected, the application schedules an appointment in Google Calendar for the event mentioned in the tweet. This tool provides an innovative way for farm event organizers to automate their event scheduling process based on social media interactions.

## Features

- Monitors Twitter for a customizable hashtag
- Automatically schedules appointments in Google Calendar based on the tweet's content
- Simple configuration and user-friendly setup

## Requirements

Before you can use this script, ensure that you have the following prerequisites installed:

- Python 3.x
- Tweepy (A Python library for accessing the Twitter API)
- A Twitter Developer account and API credentials
- Google Calendar API client library
- OAuth 2.0 credentials for Google Calendar API

## Installation

Follow these steps to install Farm Scheduler:

1. Clone the repository or download the ZIP file and extract it.
2. Open your terminal and navigate to the script's directory.
3. Install the required Python dependencies using pip:

```bash
pip install -r requirements.txt
```

    Rename config_sample.py to config.py and populate it with your Twitter API credentials, Google Calendar API credentials, and the desired hashtag.

## Configuration

Edit the config.py file with your specific settings:

   - CONSUMER_KEY: Your Twitter API consumer key
   - CONSUMER_SECRET: Your Twitter API consumer secret
   - ACCESS_TOKEN: Your Twitter API access token
   - ACCESS_TOKEN_SECRET: Your Twitter API access token secret
   - HASHTAG: The hashtag you want to monitor (e.g., #FarmEvent)
   - Google Calendar API settings as outlined in the API's documentation

## Usage

Run the Farm Scheduler with the following command:

```bash

python farm_scheduler.py
```

## How It Works

Farm Scheduler utilizes the Tweepy library to stream live tweets containing the chosen hashtag. Once identified, the tweet is parsed for details about the event, and these details are used to create an appointment in your Google Calendar using Google's Calendar API.