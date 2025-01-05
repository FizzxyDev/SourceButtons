<h1 align="center">Hai aku Fizzxy! <img src="https://user-images.githubusercontent.com/1303154/88677602-1635ba80-d120-11ea-84d8-d263ba5fc3c0.gif" width="40px" alt="Hamlo"><br></h1>

```
You Visitors To:
```
![](https://komarev.com/ghpvc/?username=FizzxyDev&label=PROFILE+VIEWS)


![My Card ](https://cardivo.vercel.app/api?name=FizzxyTheGreat%20&description=”aku%20hanya%20bisa%20memprogram%20nya%20jika%20kodenya%20sudah%20benar%20program%20itu%20akan%20berjalan%20sesuai,%20keinginan%20pemilik%20aslinya”%20(%20tapi%20ini%20bukan%20soal%programnya%20)&image=https://b.top4top.io/p_2090f6xvx0.jpg&backgroundColor=%23ecf0f1&instagram=@wfizzx&github=FizzxyDev&pattern=leaf&colorPattern=%23eaeaea)

___

<p align="center">

  <a href="https://github.com/FizzxyDev"><img title="Author" src="https://img.shields.io/badge/Author-FizzxyDev-red.svg?style=for-the-badge&logo=github" /></a>



</p>
<audio autoplay="true" src="https://f.top4top.io/m_2092qvkoa0.mp3"></audio>

## Hii i'm Fizzxy 👋
## Using @fizzxydev/baileys-pro

## NpmJs: [Click Here](https://www.npmjs.com/package/@fizzxydev/baileys-pro)

## Buttons Message:
```
// send old a buttons
client.sendMessage(m.chat, {
     text: "Hello World !",
     footer: "Fizzxy - 2025",
     buttons: [ 
         { buttonId: `🚀`,
          buttonText: {
              displayText: '🗿'
          }, type: 1 }
     ],
     headerType: 1,
     viewOnce: true
 },{ quoted: null })
 ```
 
## send location buttons:
```
client.sendMessage(m.chat, {
  location: {
    degreesLatitude: -6.2088, // Ganti dengan latitude lokasi
    degreesLongitude: 106.8456, // Ganti dengan longitude lokasi
  },
  caption: "Ini adalah lokasi yang dikirim.",
  footer: "© FizzxyTheGreat",
  buttons: [
          { buttonId: `🚀`,
          buttonText: {
          displayText: '🗿'
          },
           type: 1 }
          ], // isi buttons nya
  headerType: 6,
  viewOnce: true
}, { quoted: m });
```


## send image buttons:
 ```
  client.sendMessage(m.chat, {
  image: { url: "LINK YOUR IMAGE" },
  caption: "Ini pesan gambar Buttons", 
  footer: "© Fizzxy Dev",
  buttons: [
    {
      buttonId: '.owner',
      buttonText: {
        displayText: 'Dev bot'
      },
      type: 1
    },
  ],
  headerType: 1,
  viewOnce: true
}, { quoted: m })
```

## send document buttons:
```
let buttonMessage = {
  document: { url: "https://www.youtube.com/" },
  mimetype: "application/vnd.openxmlformats-officedocument.wordprocessingml.document",
  fileName: "「 FizzxyTheGreat 」",
  fileLength: 999,
  pageCount: 999,
  contextInfo: {
    forwardingScore: 555,
    isForwarded: true,
    externalAdReply: {
      mediaUrl: "https://www.youtube.com/",
      mediaType: 2,
      previewType: "pdf",
      title: "kamu mana punya",
      body: "ini", 
      thumbnail: fs.readFileSync("./path/to/image"),
      sourceUrl: "https://www.youtube.com/",
    },
  },
  caption: "tes",
  footer: "2020",
  buttons: [
    {
    buttonId: "ID MU", 
    buttonText: { 
      displayText: 'Display text' 
    }
  }, {
    buttonId: "ID MU", 
    buttonText: {
      displayText: "DISPLAY TEXT"
    }
  }
  ],
  viewOnce: true,
  headerType: 6,
};

return await client.sendMessage(m.chat, buttonMessage, { quoted: null });
```

## send all buttons interactive:
 ```
const { generateWAMessageFromContent, proto } = require("@FizzxyDev/BaileysPro")
let msg = generateWAMessageFromContent(m.chat, {
  viewOnceMessage: {
    message: {
        "messageContextInfo": {
          "deviceListMetadata": {},
          "deviceListMetadataVersion": 2
        },
        interactiveMessage: proto.Message.InteractiveMessage.create({
          body: proto.Message.InteractiveMessage.Body.create({
            text: "Fizzxy Dev"
          }),
          footer: proto.Message.InteractiveMessage.Footer.create({
            text: "Bot"
          }),
          header: proto.Message.InteractiveMessage.Header.create({
            title: "Igna",
            subtitle: "test",
            hasMediaAttachment: false
          }),
          nativeFlowMessage: proto.Message.InteractiveMessage.NativeFlowMessage.create({
            buttons: [
              {
                "name": "single_select",
                "buttonParamsJson": "{\"title\":\"title\",\"sections\":[{\".menu\":\".play dj webito\",\"highlight_label\":\"label\",\"rows\":[{\"header\":\"header\",\"title\":\"title\",\"description\":\"description\",\"id\":\"id\"},{\"header\":\"header\",\"title\":\"title\",\"description\":\"description\",\"id\":\"id\"}]}]}"
              },
              {
                "name": ".menu",
                "buttonParamsJson": "{\"display_text\":\"quick_reply\",\"id\":\"message\"}"
              },
              {
                 "name": "cta_url",
                 "buttonParamsJson": "{\"display_text\":\"url\",\"url\":\"https://www.google.com\",\"merchant_url\":\"https://www.google.com\"}"
              },
              {
                 "name": "cta_call",
                 "buttonParamsJson": "{\"display_text\":\"call\",\"id\":\"message\"}"
              },
              {
                 "name": "cta_copy",
                 "buttonParamsJson": "{\"display_text\":\"copy\",\"id\":\"123456789\",\"copy_code\":\"message\"}"
              },
              {
                 "name": "cta_reminder",
                 "buttonParamsJson": "{\"display_text\":\"Recordatorio\",\"id\":\"message\"}"
              },
              {
                 "name": "cta_cancel_reminder",
                 "buttonParamsJson": "{\"display_text\":\"cta_cancel_reminder\",\"id\":\"message\"}"
              },
              {
                 "name": "address_message",
                 "buttonParamsJson": "{\"display_text\":\"address_message\",\"id\":\"message\"}"
              },
              {
                 "name": "send_location",
                 "buttonParamsJson": ""
              }
           ],
          })
        })
    }
  }
}, {})

return client.relayMessage(msg.key.remoteJid, msg.message, { messageId: msg.key.id })
```

## buttons double:
```
client.sendMessage(m.key.remoteJid, {
  text: "Hello Wolrd !;", 
  footer: "© Fizzxy Dev",
  buttons: [
    { 
      buttonId: '.owner', 
      buttonText: { displayText: 'Dev bot' }, 
      type: 1,
      viewOnce: true
    },
    { 
      buttonId: 'huu', 
      buttonText: { displayText: '\nSaya pedo:v' }, 
      type: 1,
      viewOnce: true
    },
    { 
      buttonId: 'action', 
      buttonText: { displayText: 'pajangan' }, 
      type: 4, 
      nativeFlowInfo: {
        name: 'quick_reply', 
        buttonParamsJson: '{"display_text":"quick_reply","id":".play a thousand year"}',
      },
      viewOnce: true
    },
    { 
      buttonId: 'cta_url', 
      buttonText: { displayText: 'Go to URL' }, 
      type: 4, 
      nativeFlowInfo: {
        name: 'cta_url',
        buttonParamsJson: '{"display_text":"url","url":"https://www.google.com","merchant_url":"https://www.google.com"}'
      },
      viewOnce: true
    }
  ],
  headerType: 1,
  viewOnce: true
}, { quoted: m });
```

