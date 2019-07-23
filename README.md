# Cboard Cordova - AAC communication board with text-to-speech for mobile devices

Clone `git clone --recursive git@github.com:nous-/ccboard.git`

This is a Cordova application that wraps the original [Cboard React application](https://github.com/cboard-org/cboard) to bring native mobile support. The Cboard react app is maintained to support Cordova detection, setup and bindings. *(Jul 2019 - React build updates not checked in yet)*

Text-to-speach (TTS) support is provided via [`phonegap-plugin-speech-synthesis`](https://github.com/macdonst/SpeechSynthesisPlugin). This plugin bridges the native operating system TTS functionality to browser app, in a way that mimics [W3C Web Speech API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API): `SpeechSynthesis`. It uses the `android.speech.tts.TextToSpeech` interface on Android.

## One-time setup

1. `git submodule update` - Get Cboard app 
1. `npm i`
1. `cordova platform add android` - Add Android Cordova platform 
1. `mkdir -p www` - Make root cordova app folder 
1. `cd cboard`
1. `npm i`

## Building

1. `cd cboard`
1. Release `npm run build` / Debug `npm run build-cordova-debug`
1. `cp -r ./build/* ../www`
1. `cd ..`
1. `cordova run android --emulator`

## Debugging output

For emulator console.log output, you can either run in the debugging under eg. `Android Studio`, or in Chrome, navigate to `chrome://inspect`, and select the remote target that shows up once the emulator starts.