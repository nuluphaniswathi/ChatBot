ChatBot Application
Prerequisites:
Install Aws-sdk using npm install aws-sdk
Process:
create instance using Aws-sdk
import that instance in required file.Here i have imported in ChatBot.js file
Integrate using that instance with specifies AWS lambda credentials like below
lexRuntimeV2.recognizeText({
            botId: process.env.REACT_APP_BOT_ID,
            botAliasId: process.env.REACT_APP_BOT_ALIAS_ID,
            localeId: process.env.REACT_APP_LOCALE_ID,
            sessionId: sessionId,
            text: inputMessage,
          })
          .promise();
I have specified all these inputs in .env file.It will vary.
Then work on UI and format messages what you want from AWS LAMDA and show it in ChatBot
