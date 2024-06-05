## Welcome to the Communitrics API Documentation
## Here you can see the different endpoints of the API, the expected responses, and the parameters available for each.
### The URL of the API is [api.communitrics.com](https://api.communitrics.com/)<br><br>

# Channel database
- `https://api.communitrics.com/` Going to the base URL gives the full [Discord bot](https://communitrics.com/invite) database. This has all records from all the channels we currently track (over 40,000 records, always growing).
 - Optional parameters:
   - **`/CHANNEL_ID` Specify a channel ID (such as UCX6OQ3DkcsbYNE6H8uQQuVA) to only retrieve records for that channel.**
   - `?averages=true` Specifying `?averages=true` in the URL includes averages in the response. These are daily, minutely and secondly averages correct to 10 decimal places.
   - `?all=true` Specifying `?all=true` in the URL includes all subscriber count records. This is not reccomended due to this including hits and re-hits for milestones (not just the first time the channel hit it), making averages sometimes be very high.
   -  `?david=true` Specifying `?david=true` in the URL provides the daily Daivd Summerall Viewstats updates for MrBeast that he did between January and April of 2024 in the response. Without specifying this, you only get the API milestones of MrBeast.
   - `?format=csv` Specifying `?format=csv` in the URL gives you a popup to download the response with your chosen paramaters as a CSV file.
 - You can choose multiple parameters by separating them with `&`. For example, `?averages=true&all=true` would include both averages and all subscriber count records in the response.
<br><br><br>

# YouTube API search
- `https://api.communitrics.com/youtube/api?channel=CHANNEL_NAME` Going to this URL gives you real-time statistics and more data of your chosen channel, directly using the YouTube API
   - **Replace `CHANNEL_NAME` with the name of your desired channel, for example `mrbeast`**
<br><br><br>

# MrBeast latest statistics
- `https://api.communitrics.com/mrbeaststats` Going to this URL gives you the latest statistics of MrBeast updated every few seconds, using his studio subscriber count provided by [Viewstats](https://viewstats.com/). This also has data like the current averages, and the amount of subscribers he's gained in the past 24 hours / since the count came out, and more! You can download this as a CSV by going to [this site](https://charlie-ashford.github.io/mrbeastGraph/) and clicking the "Export Data to CSV" button.
<br><br><br>

# MrBeast realtime statistics
- `https://api.communitrics.com/mrbeast` Going to this URL gives you the full statistics of MrBeast updated every few seconds / minutes, using his studio subscriber count provided by [Viewstats](https://viewstats.com/). You can download this as a CSV by going to [this site](https://charlie-ashford.github.io/mrbeastGraph/) and clicking the "Export Data to CSV" button.
<br><br><br>

# Bot statistics
- `https://api.communitrics.com/stats` Going to this URL gives you the statistics of the Discord bot, like how many channels are currently being tracked, the total combined subscriber count and more!.
<br><br><br>

# Global counter
- `https://api.communitrics.com/counter` Going to this URL gives you the real-time count of a [global counter](https://charlie-ashford.github.io/globalCounter/) I made.
<br><br><br>

# Channels being tracked
- `https://api.communitrics.com/channels` Going to this URL gives you a list of all the YouTube channel ids that Communitrics is currently tracking.
 - Optional parameters:
   - `/discordServerID` Specify a Discord server ID (such as 1247883047941181450) to see all the YouTube channels that a Discord server is currently tracking.
   - `?format=csv` Specifying `?format=csv` in the URL gives you a popup to download the response with your chosen paramaters as a CSV file.
<br><br><br>
