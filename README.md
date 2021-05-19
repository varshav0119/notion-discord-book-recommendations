# Notion-Discord Book Recommendations

## About the Integration 
This is a Discord bot that ports book recommendations from Discord to Notion. Here is a simple diagram to illustrate what the bot does!
![Could not Load Diagram](https://github.com/FruitVodka/notion-discord-sync/blob/main/examples/notion-discord-sync/flow-diagram.png)

This integration works using an unofficial Python SDK for the [Notion API](hhttps://developers.notion.com/), which can be found at [notion-sdk-py](https://github.com/ramnes/notion-sdk-py).

## Try it Yourself
To test this Discord bot, you will need to set up a few things:

### Notion Reading List Database Template
You can duplicate [this](https://www.notion.so/e2b278fd05574df694833e6790e02340?v=34c458559056411d8cbd3bc3a7f406d6) template for running this example. You need to create a Notion integration as explained in the Notion API documentation [here](https://developers.notion.com/docs).
After doing this, you will obtain a **Notion Internal Integration Token** and a **database ID**. Note these down somewhere secure to use later.

### Discord Bot
Follow the instructions [here](https://realpython.com/how-to-make-a-discord-bot-python/) to create a Discord Bot and add it to your server. Make sure to give the bot permissions to view the channel(s) where book recommendations will be coming in! At the end of this, you will obtain a **Discord Bot Token**. Note this down too.

### Google Books API
Create a GCP project and get your **Google Books API credentials** by following [these](https://developers.google.com/books/docs/v1/using) instructions.

### Running the Bot
1. Clone this repository locally: `git clone hhttps://github.com/FruitVodka/notion-discord-book-recommendations.git`
3. Add the credentials from the previous sections to a `.env` file in `src`; the file should look like the below:
```
DISCORD_TOKEN={discord-bot-token}
DISCORD_GUILD={discord-server-name}
NOTION_TOKEN={notion-integration-token}
DATABASE_ID={notion-database-id}
BOOKS_API_KEY={google-books-api-key}
```
4. Install the requirements in `requirements.txt` by running the command `pip3 install -r requirements.txt` in the project root directory
5. Run `bot.py` - it contains the code that powers this Discord bot

## Resources
* [Notion API Documentation](https://developers.notion.com/reference/intro)
* [notion-sdk-py](https://github.com/ramnes/notion-sdk-py)
* [discord.py](https://github.com/Rapptz/discord.py)
* If you want to use your own database instead of using the provided template, you might find [this](https://developers.notion.com/reference/page#page-property-value) description of the `page object` in Notion useful.

## Contributing
This is a work-in-progress. To contribute, fork this repository and raise a pull request. Feedback and suggestions are welcome, please head to the Discussions section to start a conversation!
