# SIPERB

Siperb sits in the cloud between your existing PBX and your users, to provide them with a state-of-the-art WebRTC enabled client endpoint (UAC).

There are various ways to connect with us if you want, or you don't even need to connect with us at all. 
It's up to you. You are welcome to use our system without connections for free, but then you must make sure that your PBX is fully WebRTC capable.

We can connect to your PBX (UAS) via our outbound registrations, or your PBX (UAS) can connect to us via our inbound registrations. 
This links us with you. You are not limited by these connections. 
You can make as many as you want. 
You will probably want to make one per extension on your PBX that you want to use with WebRTC. 
One of these connections can also be a TISP, like Twillio Elastic SIP Trunking. 
You are also not limited to the number of devices you can register your client endpoint (UAC) with.

## Mobile App Objectives

The primary concept of this project is to build a WebView that can contain the HTML and JavaScript necessary to perform any of the task necessary for the Browser/WebRTC Phone to work. 

Special attention is applied to features that are typical of a mobile device. For instance, unlike a Desktop computer, a mobile device is used for (many) shorter periods during a typical day. Each time the screen is on, or the device is in use, its making use of the battery. It is of utmost important to keep the battery use to a minimum. Mobile operating systems go to extreme lengths to preserve battery power especially if the app is not in the foreground, or actually being used. You can see this by simply refraining from scrolling, and touching the screen for a few seconds - you should see the screen dim, or turn off. A few seconds after that, all network activity is shut down (except push notification communications).

It is the objective of the mobile apps, to provide all the necessary (natively coded) functionality outside of core calling functionality. 

This will include:

### Network monitoring

The mobile app will be responsible for monitoring the sate of connectivity for the device, and inform the webview of possible changes so that it can register or re-register.

### Rotation Handling

Unlike a desktop computer, a mobile device can be easily rotated in your hand. They are also (often) fitted with a gyroscope, that allows the application to know the rotation of the device, and therefor the screen. This is important because the screen is typically not square, and has a big impact of the layout of elements on the page. The Application so handle the rotation and limit the screen drawing to portrait for the majority of the time, unless the user has selected a Fullscreen video conference. 

### Proximity Handling

Unlike a desktop computer, a mobile device can be easily moved around, and especially when the user moves the device to their ear. This action should automatically set the device to a suitable sound output, and then moving the device away from your ear should again change the device back to an appropriate output and should level.

### Audio Device Handling (including bluetooth)

### Ring Tones and Personalisation

### Local Storage and Sync State Handling

### Contact Intergration

### Camera & Microphone permission

### Incoming Call Notification
