# SIPERB - WebRTC Softphone

Siperb Services sits in the cloud between your existing PBX and your users, to provide them with a state-of-the-art SIP-based [Softphone](https://www.siperb.com/kb/article/softphone/) powered by [WebRTC](https://www.siperb.com/kb/article/what-is-webrtc/).

## SIP Proxy for Asterisk, FreeSWITCH or any SIP-based PBX

Siperb's [SIP Proxy](https://www.siperb.com/kb/article/webrtc-to-sip-proxy/) then provides the nessesary routing to connect the [Web Application or Mobile Application](https://www.siperb.com/kb/article/siperb-webrtc-client-web-tablet-and-mobile/) to your PBX. Inbound calls are notified via Push for both mobile and web. Outbound calls are routed via connections, to your own PBX like Asteriks, FreeSWITCH or any SIP based IP PBX.

There are various ways to [connect](https://www.siperb.com/kb/topics/connections/) with us if you want, or you don't even need to connect with us at all. 
It's up to you. You are welcome to use our system without connections for free, but then you must make sure that your PBX is fully WebRTC capable.

We can connect to your PBX (UAS) via our outbound registrations, or your PBX (UAS) can connect to us via our inbound registrations. 
This links us with you. You are not limited by these connections. 
You can make as many connections as you want. 
You will probably want to make one per extension on your PBX that you want to use with WebRTC. 
One of these connections can also be a TISP, like Twillio Elastic SIP Trunking. 
You are also not limited to the number of devices you can register your client endpoint (UAC) with.

## Windows Softphone | Mac Softphone | Linux Softphone

While Siperb is a web-based softphone, it is also 100% PWA compatible, so this means that you can install Siperb from the browser and run Siperb as a Desktop Applicaiton on Windows, Mac, and Linux.

![Siperb](https://github.com/Siperb/.github/blob/main/profile/Recording_Format.webp?raw=true)

## Apple & Androind Mobile Softphone Application

Special attention is applied to features that are typical of a mobile device. For instance, unlike a Desktop computer, a mobile device is used for (many) shorter periods during a typical day. Each time the screen is on, or the device is in use, its making use of the battery. It is of utmost important to keep the battery use to a minimum. Mobile operating systems go to extreme lengths to preserve battery power especially if the app is not in the foreground, or actually being used. You can see this by simply refraining from scrolling, and touching the screen for a few seconds - you should see the screen dim, or turn off. A few seconds after that, all network activity is shut down (except push notification communications).

It is the objective of the mobile apps, to provide all the necessary (natively coded) functionality outside of core calling functionality. 

- [Downlaod Android Softphone in Play Store](https://play.google.com/store/apps/details?id=com.siperb.mobile)
- [Downlaod Apple Softphone in App Store](https://apps.apple.com/us/app/siperb/id6553983983)

This will include:

### Network monitoring

The mobile app will be responsible for monitoring the sate of connectivity for the device, and inform the webview of possible changes so that it can register or re-register.

### Rotation Handling

Unlike a desktop computer, a mobile device can be easily rotated in your hand. They are also (often) fitted with a gyroscope, that allows the application to know the rotation of the device, and therefor the screen. This is important because the screen is typically not square, and has a big impact of the layout of elements on the page. The Application so handle the rotation and limit the screen drawing to portrait for the majority of the time, unless the user has selected a Fullscreen video conference. 

### Proximity Handling

Unlike a desktop computer, a mobile device can be easily moved around, and especially when the user moves the device to their ear. This action should automatically set the device to a suitable sound output, and then moving the device away from your ear should again change the device back to an appropriate output and should level.

### Missed Event Badge

For mobile apps, the app icon normally supports some sort of missed event notification. This could be a call, or any message. On reading the message, the notification can be reduced or removed.

### Audio Device Handling (including bluetooth)

The mobile application should take on the role of audio device manager, allowing the user to plug in a headset or microphone, and have it automatically be avaialbe to use (or use automatiacly if the preference is set). These divcies must not be limited to plugin devices, they should unclude Bluetooth, and car audio devices. 

### Ring Tones and Personal Settings

The user should be presented with a list of system ring tones, allowing the device to audibly ring much like a typical GSM call. The user must be able to select the ring tone, and set other personalisation specific to this device. These settings should be stored locally on the device. These settings are different to the provisioned settings that may be common to all instances of the users account. 

### Local Storage and Sync State Handling

Should the user select the paid-for options, all data should be synced to their online Control Panel. Embedded JavaScript will perform these tasks, however the state of sync and progress of this should be reported easily to the user.

### Contact Integration

Most of the time, users save their contacts to their mobile phones, and/or make use of services like iCloud, Google etc for maintaining contacts. In most cases the mobile devices is a central location for all the users contacts (synced or static), this provides an opportunity for the mobile app to make use of these contacts. The mobile app would have its own "roster" of contacts with full history, but would still require a user to copy over (or reference) a contact from the users contacts. (This is the same as WhatsApp). The mobile app is required to perform the task of handling reference between stored contacts in the users phone, and contacts on the mobile app.

### Camera & Microphone permission

It should be the responsibility of the mobile app to obtain the necessary permission to use the camera and microphone. The actual UI for the request can be done in the Browser UI, but the request should be handled in native code.

### Incoming Call Notification

For both Android and iOS, incoming call notifications should be handled from the push notifications service. If the user select the option, a push notifications will be sent to the device prior to each incoming call. It will be the responsibility of the mobile app to accept this push notification, wake the application, register the extension, and bring the application to the foreground. Once the application is registered, the call will be sent to the device, and a regular inbound call flow can continue. It should be noted that at this point, it may be possible that the users phone is still locked, and/or the application is not the front-most, so this may present permission difficulties. Android and iOS have different approaches to this function, and user privacy would be a consideration. A best possible solution - similar to the regular GSM call, or like WhatsApp, should be reached.
