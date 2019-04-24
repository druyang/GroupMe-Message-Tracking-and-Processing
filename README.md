Originally created to track the number of trivia points given by one user to another user. 

This is a tool to download GroupMe messages from a groupchat to a CSV file and processes the messages. 
This includes tracking the number of times certain phrases are mentioned.  


Fork of / Based off of: 
youyanggu/groupme_stats


Getting Access Token
--------------
In order to download GroupMe messages, you need an unique access token provided to you by GroupMe. To get this, log into GroupMe's <a href="https://dev.groupme.com/session/new" target="_blank">Developers</a> website and click Access Token on the upper right. You should then be given a 32-character or 40-character access token. You will need this later.

Dependencies
--------------
Python 2.7. You need to have Python's <a href="http://docs.python-requests.org/en/latest/" target="_blank">requests</a> library: ```pip install requests```

Instructions
--------------
1. Get your GroupMe Access Token using the instructions above.
2. Run ```python retrieve_msgs.py```, pass in your access token, and follow the command line interface to download your GroupMe messages to a CSV file. Use ```python retrieve_msgs.py --help``` to see a list of commands. Below are some sample usages:
  - ```python retrieve_msgs.py <YOUR ACCESS TOKEN> -a -c output.csv``` will output all of your GROUP messages into a csv file called output.csv.
  - ```python retrieve_msgs.py <YOUR ACCESS TOKEN> -g "Beer League Hockey"``` will output your GROUP messages from the Beer League Hockey group into a csv file called beer_league_hockey.csv.
  - ```python retrieve_msgs.py <YOUR ACCESS TOKEN> -d -a``` will output all of your DIRECT MESSAGES into a separate csv file for each person.
  - ```python retrieve_msgs.py <YOUR ACCESS TOKEN> -d -g "Jennifer Lawrence" -c jlaw.csv``` will output your DIRECT MESSAGES from Jennifer Lawrence into a csv file called jlaw.csv.
3. Run ```python run_stats.py``` and pass in your CSV file to display some simple stats about your messages. Use ```python run_stats.py --help``` to see a list of commands. For example: ```python run_stats.py output.csv``` will simply give you the number of messages sent by each individual.

If you run into any issues running this, let me know via the "Issues" tab. Some of the code is not fully tested so please file a bug report if an error occurs and I will try to address it!
