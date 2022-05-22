# discord-timeout.js

discord-timeout.js is a Node.js library for working with discord.js
## Installation

Use the package manager [npm](https://www.npmjs.com/) to install  discord-timeout.js.

```bash
npm i discord-timeout.js
```
## Usage

```javascript
const Discord = require('discord.js')
const client = new Discord.Client();
const timeout = require('discord-timeout.js')
timeout(client)
client.on('ready', () => {
  console.log('redy')
})
client.on("message",async(message)=>{
        if(message.content == "test"){
                new timeout.Timeout(message.guild ,message.author, "30sec")
        }
})
client.login(process.env.TOKEN)
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

