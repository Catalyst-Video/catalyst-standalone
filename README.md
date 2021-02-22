# Catalyst - Drop In WebRTC Group Video Chat

- (Semi-Functional) Screen sharing
- Text chat
- Live captions
- Group video calls with up to 10 people

## Requirements

- Node 10/12

#### Setting up credentials

- Get Account SID and Auth Token from the Twillio console
- Fill in all .env.template fields and rename it to .env

#### Install dependencies

```
npm i
```

#### Start the server (Catalyst instance)

```
npm start
```

# Drop In Config

# Sending Arbitrary Data

Call the window's sendArbitraryData function and give it a string representation of the message you want to send. All connected clients will receive this data and it will be available in the "arbitrary-data" element on the document root.

## Headers

"msg:" + A text message sent over the data channel
"cap:" + A caption update sent over the data channel

### URL Parameters (Drop In)

| url param              | value  | description                                                                                |
| ---------------------- | ------ | ------------------------------------------------------------------------------------------ |
| hide_chat              | true   | hides the chat by default                                                                  |
| join_message           | string | displays this message instead of the default copy link to join message when joining a room |
| hide_join_copy_message | true   | replace "copy link" button in join message with a "dismiss" button                         |
