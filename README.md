*Prerequisites
AWS SDK: Install the AWS SDK by running:
npm install aws-sdk
Process Overview
1.Create an AWS SDK Instance: Set up an instance using the AWS SDK. This instance will be used to communicate with AWS Lex and Lambda.

2.Import the AWS SDK Instance: Import this instance into the required file, such as ChatBot.js, to handle interactions with AWS services.

3.Integrate with AWS Lex: Use the instance to connect with AWS Lex using specified AWS Lambda credentials as shown below:

lexRuntimeV2.recognizeText({
    botId: process.env.REACT_APP_BOT_ID,
    botAliasId: process.env.REACT_APP_BOT_ALIAS_ID,
    localeId: process.env.REACT_APP_LOCALE_ID,
    sessionId: sessionId,
    text: inputMessage,
}).promise();

4.All necessary credentials are stored in the .env file to keep sensitive information secure. Customize these values according to your environment.
5.Build the UI: Develop the user interface for the chatbot and format the responses to display messages returned by AWS Lambda.

This setup creates a seamless chatbot experience, allowing users to interact dynamically with AWS Lex through a custom UI.


