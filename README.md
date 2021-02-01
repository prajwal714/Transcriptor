<!-- <h1 align="center" style="border-bottom: none;">🎤 Transcriptor </h1>
<h3 align="center">Node.js sample applications that shows some of the the IBM Watson Speech to Text service to translate a zoom meeting to notes.</h3>
<p align="center">
  <a href="http://travis-ci.org/watson-developer-cloud/speech-to-text-nodejs">
    <img alt="Travis" src="https://travis-ci.org/watson-developer-cloud/speech-to-text-nodejs.svg?branch=master">
  </a>
  <a href="#badge">
    <img alt="semantic-release" src="https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg">
  </a>
</p>
</p> -->

The [Transcriptor][service_url] service uses IBM's speech recognition capabilities to convert speech in multiple languages into text. The transcription of incoming audio is continuously sent back to the client with minimal delay, and it is corrected as more speech is heard. The service is accessed via a WebSocket interface; a REST HTTP interface is also available; It has an integrated Zoom Meeting SDK to attend meeting and stream the meeting audio directly to the IBM speech to text service.

## Prerequisites

1. Sign up for an [IBM Cloud account](https://cloud.ibm.com/registration/).
1. Download the [IBM Cloud CLI](https://cloud.ibm.com/docs/cli?topic=cloud-cli-getting-started#overview).
1. Create an instance of the Speech to Text service and get your credentials:

   - Go to the [Speech to Text](https://cloud.ibm.com/catalog/services/speech-to-text) page in the IBM Cloud Catalog.
   - Log in to your IBM Cloud account.
   - Click **Create**.
   - Click **Show** to view the service credentials.
   - Copy the `apikey` value.
   - Copy the `url` value.

1. Create a zoom marketplace account
1. Get your Zoom API secret key and URL

## Configuring the application

1. In the application folder, copy the _.env.example_ file and create a file called _.env_

   ```
   cp .env.example .env
   ```

2. Open the _.env_ file and add the service credentials that you obtained in the previous step.

   Example _.env_ file that configures the `apikey` and `url` for a Speech to Text service instance hosted in the US East region:

   ```
   SPEECH_TO_TEXT_IAM_APIKEY=X4rbi8vwZmKpXfowaS3GAsA7vdy17Qh7km5D6EzKLHL2
   SPEECH_TO_TEXT_URL=https://api.us-east.speech-to-text.watson.cloud.ibm.com
   REACT_APP_ZOOM_API_KEY=sample_api_key
   REACT_APP_ZOOM_API_SECRET_KEY=sample-secret-key
   ```

## Running locally

1. Install the dependencies

   ```
   npm install
   ```

1. Run the application

   ```
   npm start
   ```

1. View the application in a browser at `localhost:3000`

## License

This Code follows all the requirements licensed under Apache 2.0.

## Open Source @ IBM

Find more open source projects on the [IBM Github Page](http://ibm.github.io/)

[service_url]: https://www.ibm.com/cloud/watson-speech-to-text
[docs]: https://cloud.ibm.com/apidocs/speech-to-text
[sign_up]: https://cloud.ibm.com/registration/?target=/catalog/services/speech-to-text/
