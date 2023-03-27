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

You may be wondering how WebRTC and Mobile work together? The primary concept of this project is to biuld a WebView that can contain the HTML and JavaScript nessesary to perform any of the taks nessesary for the Browser/WebRTC Phone to work. 

Specail attention is applied to features that are typical of a mobile device. For instance, unlike a Desktop computer, a mobile device is used for (many) shorter periods during a typical day. Each time the screen is on, or the device is in use, its making use of the battery. It is of utmost importants to keep the battery use to a minimum. Mobile opperating systems go to extream lenghts to perseve battery power especially if the app is not in the forground, or actually being used. You can see this by simply refaining from scrolling, and touching the screen for a few seconds - you should see the screen dim, or turn off. A few seconds after that, all network activity is shut down (except push notification communications).

It is the objectibve of the mobile apps, to provide all the nessesary (nativly coded) functionaliy out side of core calling functionaliy. 

This will iclude:

## Network monitoring

The mobile app will be responsible for monitoring the sate of connectivity for the device, and inform the webview of possible changes so that it can register or re-register.
