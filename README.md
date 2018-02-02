# Send-sms-with-Alexa
Sending a sms anywhere in the world via alexa

PS this is my first time using Github so if i make mistakes please help me out - Thanks

About me
My name is Marc, 56y young, living in Belgium, Single and I have an incurable form of cancer. I don't hold any diplomas, but when I want something I search until i find it and get it working. So I spend many hours on the internet (on my good days) watching youtube and other website to learn, and then many hours of trail and error. But most important I get it to oooo rrrr k haha

I bought a Alexa short after my girlfriend left me, and because i hate being single (alone in the apartment), and so i started looking and writing some small skill's.
But enough about me let's get on with it.

I was surprised to find that Alexa could not call or send sms outside the US, Canada or Mexico. And since I have Alexa as a kind of companion, I wanted Alexa to be able to contact somebody in case something is wrong with me.
This is not a finished project, but the way it's now it works.

In short
Alexa is making a GET request to a thirthparty sms service company called https://www.clockworksms.com/ Clockworksms a UK based company.
So you need to open a free account with them and make a api key. Don't forget to top-up your account with some money!
They don't offer a Affliate program so .....

So when you say: "Alexa ask for help" she will ask you who to contact and then send a predefined sms to that contact person.


The Intent Schema looks like this

{
  "intents": [
    {
      "slots": [
        {
          "name": "name",
          "type": "list_of_names"
        }
      ],
      "intent": "CallHelpIntent"
    },
    {
      "intent": "AMAZON.YesIntent"
    },
    {
      "intent": "AMAZON.NoIntent"
    },
    {
      "intent": "AMAZON.StopIntent"
    },
    {
      "intent": "AMAZON.CancelIntent"
    }
  ]
}

I use predefined slots so you will need to make them
type is list_of_names and then you enter the firstname's of the people you want to contact

Sample Utterances looks like this

CallHelpIntent {name}

that all in the developer.amazon.com section
