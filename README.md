<div align="center">
  <p>
    <h1>Discord.JS v13</h1>
  </p>
</div>

## Introduction. & บทนำ.

***
Here's an example of a bot project being developed with. Discord.JS Version 13 which is the latest version.

นี่คือตัวอย่างโปรเจคบอทที่ถูกพัฒนาด้วย ดิสคอร์ด.เจเอส เวอร์ชั่น13 ซึ่งเป็นเวอร์ชั่นใหม่ล่าสุด
***

## How To Setup & วิธีการตั้งค่า

[Build a Discord Bot with Discord.js (v13)](https://dev.to/hypening/build-a-discord-bot-with-discord-js-v13-14mj)

[สร้าง Discord Bot ด้วย Discord.js (v13)](https://dev.to/hypening/build-a-discord-bot-with-discord-js-v13-14mj)

[Discordjs](https://discord.js.org/#/)

[Nodejs](https://nodejs.org/en/)

##Adding a command. & การเพิ่มคำสั่ง.
###You can simply add a command in the specific folder with the code below:
```javascript
const { Client, Message, MessageEmbed } = require('discord.js');

module.exports = {
    name: 'ping',
    /** 
     * @param {Client} client 
     * @param {Message} message 
     * @param {String[]} args 
     */
    run: async(client, message, args) => {
        message.channel.send('pong');
    }
}
```
###คุณสามารถเพิ่มคำสั่งในโฟลเดอร์เฉพาะด้วยรหัสด้านล่าง: 

```javascript
const { Client, Message, MessageEmbed, MessageButton } = require('discord.js');
module.exports = {
    name: 'ping',
    /** 
     * @param {Client} client 
     * @param {Message} message 
     * @param {String[]} args 
     */
    run: async (client, message, args) => {
        const row = new MessageActionRow()
            .addComponents(
                new MessageButton()
                    .setCustomId('primary')
                    .setLabel('Primary')
                    .setStyle('PRIMARY')
            );

        const embed = new MessageEmbed()
            .setColor('#0099ff')
            .setTitle('Some title')
            .setURL('https://discord.js.org')
            .setDescription('Some description here');

        await message.reply({ content: 'Pong!', ephemeral: true, embeds: [embed], components: [row] });
    }
} }
}
```
###### This project is created for educational purposes only. If there is any error, you can inquire at [Support](discord.gg/ZWmJVExdbR)
###### โปรเจคนี้สร้างขึ้นเพื่อการศึกษาเท่านั้น หากมีข้อผิดพลาดทางใดสามารถสอบถามได้ที่ [Support](discord.gg/ZWmJVExdbR)
 

