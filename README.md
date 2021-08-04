# IITD-Bot

Discord bot to administer IITD'20 Acad Server

## Commands
* `hello` to check if bot is online
* `?help` to display this message
* `?set <kerberos>` to set your kerberos and automatically assign role for branch, hostel and courses
* `?courses <kerberos>` to list courses by kerberos id
### Manager only
* `?checkmail` to track circular emails on that channel every minute
* `?update` to update roles for all registered users
* `?reload` to reload the database from `.csv` and `.json` files

## Configure
* Install python then clone this repo and switch into the directory
* Install dependencies `discord`, `bs4`, `dotenv`, `requests`
* Put `BOT_TOKEN`, `IITD_EMAIL`, `IITD_PASS` in `.env` file in the same directory
* Requires files `kerberos.csv`, `hostels.csv`, `branches.csv`, `courses.csv` in the same directory to store configuration and data for the batch of your server. These are excluded in `.gitignore` for privacy reasons. Contact me if you need them for configuration.
* `course_lists.json` can be generated from `get_course_lists()` function of `utils.py` if you are connected to IIT Delhi Internal Network
* `discord_ids.json` will be generated and updated by the script
* Run `python bot.py`