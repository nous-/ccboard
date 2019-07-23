# Cboard Cordova - AAC communication board with text-to-speech for mobile devices

This is a Cordova application that wraps the original [Cboard React application](https://github.com/cboard-org/cboard) to bring native mobile support. The Cboard react app is maintained to support Cordova detection, setup and bindings.

Text-to-speach (TTS) support is provided via [`phonegap-plugin-speech-synthesis`](https://github.com/macdonst/SpeechSynthesisPlugin). This plugin bridges the native operating system TTS functionality to browser app, in a way that mimics [W3C Web Speech API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API): `SpeechSynthesis`. It uses the `android.speech.tts.TextToSpeech` interface on Android.

## Building

1. Get latest Cboard `git submodule update`
1. `cd cboard`
1. `npm run build` or `npm run build-cordova-debug` for better debug logging
1. `cp -r ./build/* ../www` Copy files into cordova folder.
1. `cd ..`
1. For Android `cordova run android --emulator`

## Debugging output

For emulator console.log output, you can either run in the debugging under eg. `Android Studio`, or in Chrome, navigate to `chrome://inspect`, and select the remote target that shows up once the emulator starts.