# A package that is helpful in bot making!
- Make commands easily using this package!

# How To Install:
- `npm i discord-utility`

# Example
```javascript
const Discord = require("discord.js");
const client = new Discord.Client();
const { Util } = require("utility-discord");
const util = new Util();
const prefix = 'Your-Prefix-Here'

client.on("message", async message => {
   if(message.content.startsWith(`${prefix}joke`)) {
      let joke = await util.fetchJoke();
      
      let embed = new Discord.MessageEmbed()
      .setTitle("Joke!")
      .setDescription(joke.title)
      .setColor("RANDOM")
      
      if(joke.body) {
         embed.setFooter(joke.body)
      }
      message.channel.send(embed)
   } else if(message.content.startsWith(`${prefix}meme`)) {
   
   let meme = await util.fetchMeme()
   
   let embed = new Discord.MessageEmbed()
   .setTitle("Meme!")
   .setDescription(meme.title)
   .setImage(meme.image)
   .setColor("RANDOM")
   message.channel.send(embed);
   
   }
});

client.login("Your Token Here");

```

# All methods and outputs. NOTE: Replace content with how you defined the method.
| Methods       | Endpoints     | Description    |
| :------------- | :----------: | -----------: |
|  fetchJoke() | content.title: Joke Title<br>content.body (If any): Joke's second part. (Will only work if there is one).| Fetch random joke.    |
| fetchMeme()   | content.title: Meme Title<br>content.image: The meme. | Fetches random meme.    |
| fetchFact() | content.fact: The fact | Fetches random fact.       |
| fetchDogFact() | content.fact: The fact | Fetches random dog fact. |
| fetchCatFact() | content.fact: The fact | Fetches random cat fact. | 
| fetchPandaFact() | content.fact: The fact | Fetches random panda fact. | 
| fetchFoxFact() | content.fact: The fact | Fetches random fox fact. | 
| fetchBirdFact() | content.fact: The fact | Fetches random bird fact. | 
| fetchKoalaFact() | content.fact: The fact | Fetches random koala fact. | 

# Will be adding more soon!
