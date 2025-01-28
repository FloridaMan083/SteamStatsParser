# SteamStat Parser: Steam Review and Concurrent User Data Visualization 

This script fetches Steam game review and concurrent user data using Steam's public APIs and plots time-series graphs to visualize trends. The graphs display review scores over time and concurrent users based on a specified game ID.

## Table of Contents

1. [Overview](#overview)
2. [Installation](#installation)
3. [Usage](#usage)
   - [Running in Google Colab](#running-in-google-colab)
   - [Running Locally](#running-locally)
4. [Parameters](#parameters)
5. [License](#license)

## Overview

The script performs the following tasks:
- Fetches game information (name and release date) using the Steam API.
- Retrieves review statistics over time, including positive review percentages and cumulative scores.
- Optionally smooths the review percentage data using a rolling mean.
- Fetches concurrent user data from SteamCharts.
- Plots the Steam review and concurrent user trends over time.

## Usage

### Running in Google Colab
You can quickly run this script in Google Colab. Follow these steps:

1. Open the Collab notebook: https://colab.research.google.com/drive/1JAWIVj1mjJPPKIpv8TB1AVh6HF88At44?usp=sharing
2. Save a copy with File > Save a Copy in Drive
3. Follow the file instructions to run

### Parameters

game_id: The Steam Store ID of the game to track (e.g., 1091500).

months_range: The number of months from the release date to track (e.g., 0 for all-time data, 6 for the last 6 months).

smooth: Set to True to apply a rolling mean to smooth the time-series data, or False to use raw data.

### Example:

game_id = 000000  # Steam Store ID of game to track

months_range = 6  # Track data for the last 6 months

smooth = True  # Apply smoothing to the time-series data

## Local Installation

To run this parser, you will need the following Python libraries:

- `requests`
- `pandas`
- `matplotlib`
- `beautifulsoup4`
- `seaborn`

You can install these libraries using pip:

```bash
pip install requests pandas matplotlib beautifulsoup4 seaborn
```

### License

This script is provided as-is. You are free to use, modify, and distribute it according to your needs
