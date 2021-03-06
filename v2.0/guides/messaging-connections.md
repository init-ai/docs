---
title: "Messaging Connections"
excerpt: ""
---
# Facebook Messenger

**Overview**

Facebook Messenger boasts over 1 billion monthly active users. It’s popularity is only growing. In the last year they opened up the Messenger platform to support bots and allow any business to take advantage of it.

**Features**

- Text
- Carousels
- Structured messages
- Persistent menu
- Rich media messages
- Images
- URL buttons
- Postback button
- Share buttons
- Buy buttons (beta)

**Integration**

1. Navigate to `Settings > Facebook Messenger` inside the project you wish to connect in the Init Console
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/01e8939-settings-detail-facebook-logged-out.png",
        "settings-detail-facebook-logged-out.png",
        1282,
        872,
        "#292c35"
      ]
    }
  ]
}
[/block]
2. Click the `Connect Facebook` to launch the Facebook oAuth pop-up
3. Run through the steps. The first step we ask for your personal Facebook information (This is required for authentication). The next step is granting access to your Pages. We need access to Pages because this is what Facebook uses for Messenger.
4. Once you're back in the Init Console, you should see some new information 
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/64f806c-settings-detail-facebook-enabled.png",
        "settings-detail-facebook-enabled.png",
        1282,
        872,
        "#292c35"
      ]
    }
  ]
}
[/block]
5. Select the Page you wish to use with your Messenger connection, and then click `Update`!

# Telegram

**Overview**

Telegram's popularity has skyrocketed over the years. While it’s not as popular as Messenger, it’s demographic is considered more tech savvy, and security oriented (Telegram encrypts all messages sent through their platform)

**Features**

- Text
- Custom keyboards
- Inline keyboards
- Images

**Integration**

1. Navigate to `Settings > Telegram` inside the project you wish to connect in the Init Console
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/d9feb2a-settings-detail-telegram-disabled.png",
        "settings-detail-telegram-disabled.png",
        1282,
        872,
        "#292c35"
      ]
    }
  ]
}
[/block]
2. Click `Create a Bot` (or navigate to the [Telegram BotFather](https://telegram.me/botfather)). You may need to log in or create an account first.

3. Run through the prompts to create a bot with the BotFather
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/103b062-settings-detail-telegram-createbot.png",
        "settings-detail-telegram-createbot.png",
        687,
        562,
        "#d5d0d5"
      ]
    }
  ]
}
[/block]
4. Once you get your `Bot Token` paste it into the `Bot Token` field in the Init Console and click `Authenticate Telegram`. If there were no errors you should see something like:

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/27eebb6-settings-detail-telegram-enabled.png",
        "settings-detail-telegram-enabled.png",
        1282,
        872,
        "#2a2d36"
      ]
    }
  ]
}
[/block]
# Twilio SMS

**Overview**

One of the largest telecom APIs, Twilio is the go-to source for connecting your services through SMS. With Init.ai you can use Twilio to deploy your conversational apps over SMS. While SMS has the most limitations (restricted to text chat and image support only) it has the potential to reach the largest audience since all you need to interact with it is a phone with SMS capabilities.

**Features**

- Text
- Images

**Integration**

1. Navigate to `Settings > Connections > Twilio` inside the project you wish to connect in the Init Console
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/c7d9ebf-settings-detail-twilio-disabled-002.png",
        "settings-detail-twilio-disabled-002.png",
        1282,
        872,
        "#292c35"
      ]
    }
  ]
}
[/block]
3. Find your Twilio Account SID and Auth Token inside your [Twilio console](https://www.twilio.com/console) under `Account summary`

4. Paste your Account SID and Auth Token into the corresponding fields in the Init Console

5. If there were no errors it should look something like this:
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/9df2097-settings-detail-twilio-enabled-001.png",
        "settings-detail-twilio-enabled-001.png",
        1282,
        872,
        "#292c35"
      ]
    }
  ]
}
[/block]
6. Once the general integration is complete, find or create a [Programmable SMS service](https://www.twilio.com/console/sms/dashboard) and copy the SID into the Messaging Service SID in the Init Console
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/927895e-settings-detail-twilio-enabled-002.png",
        "settings-detail-twilio-enabled-002.png",
        1282,
        872,
        "#eeeff1"
      ]
    }
  ]
}
[/block]
7. Next we'll have to tell Twilio where to route replies from Init. To do this, click into your Messaging SID in the [Twilio SMS dashboard](https://www.twilio.com/console/sms/dashboard) and paste this URL into the `Request URL` field `https://api.init.ai/api/v1/webhook/twilio/messaging`
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e964021-twilio-inbound-settings.gif",
        "twilio-inbound-settings.gif",
        480,
        133,
        "#e5e4e5"
      ]
    }
  ]
}
[/block]
8. That should be it! Try texting the number associated with that Messaging Service SID to verify it's connected

# Twilio Programmable Chat
[block:callout]
{
  "type": "info",
  "title": "IP Messaging",
  "body": "The Programmable Chat product was previously known as IP Messaging"
}
[/block]
**Overview**

[Twilio Programmable Chat](https://www.twilio.com/chat) enables you to completely control your conversational app experience. Using Programmable Chat you can build a chat application to live anywhere. On the web, Android, or iOS.

**Features**

- High customizability
- Text
- Images

**Integration**

 If you are interested in using Programmable Chat in your project, <a href='mailto:support@init.ai'>contact our support team</a>.


# Smooch

**Overview**

Smooch is a messaging channel aggregator. They build the connections to many of the most popular messaging channels, support platforms, and business systems. We offer a simple oAuth connection to Smooch so you can connect your current account, or create a new one.

**Features**

- Connect to many messaging channels
- Web, iOS, Android SDKs
- Ability to monitor conversations in Slack

**Integration**

> **Important Note** You will only be able to enable Smooch if you do not have an active Facebook or Telegram connection through Init.ai. Smooch offers similar integrations which will conflict with Init's connections.

1. Navigate to `Settings > Connections > Smooch` inside the project you wish to connect in the Init Console
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/297b47e-settings-detail-smooch-disabled.png",
        "settings-detail-smooch-disabled.png",
        1282,
        872,
        "#292c35"
      ]
    }
  ]
}
[/block]
2. Click the `Connect Smooch to Init` button and select the Smooch App you wish to connect to (Or create an account if you don't have a smooch account)
[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7b8a7bc-settings-detail-smooch-oauth-001.png",
        "settings-detail-smooch-oauth-001.png",
        1282,
        872,
        "#2c2f38"
      ]
    }
  ]
}
[/block]
3. Next click `Allow` to give Init access to your Smooch connections

4. From here on out you'll use Smooch to manage your integrations