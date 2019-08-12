# Intro to getUserMedia API

- getUserMediaAPI is one of the APIs derived from the WebRTC project

- getUserMedia API provides access to multimedia streams (video, audio, or both) from local devices.

## Use cases of this API

- real-time communication, also, recording tutorials or lessons for online courses
- surveillance of our home or workplace

## How it works?

- API exposes to only one method, **getUserMedia()**, that belongs to the **window.navigator** object. The method accepts as its parameters an object of constraints, a success callback, and a failure callback.
- The **constraints** parameter is an object having either one or both the properties **audio** and **video**.
- The value of these properties is a Boolean, where **true** means request the stream (audio or video), and **false** doesn't request the stream. So, to request both audio and video, we pass the following object.

```
{
    video: true,
    audio: true
}
```

Regarding the scripting part, we first test for browser support. If the API isn’t supported, we display the message “API not supported”, and disable the two buttons. If the browser supports the getUserMedia API, we attach a listener to the click event of the buttons. If the “Play demo” button is clicked, we test if we’re dealing with an old version of Opera because of the issues described in the previous section. Then, we request the audio and video data from the user’s device. If the request is successful, we stream the data using the video element; otherwise, we show the error that occurred on the console. The “Stop demo” button causes the video to be paused and the streams to be stopped.
