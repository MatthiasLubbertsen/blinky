# Blinky 👀

A lovely screensaver pet with animated eyes that follows faces using your phone's camera!

<img src="docs/assets/blinky_eyes.gif" alt="Blinky in Action"/>

## What's this?

Blinky is a fun little web-based screensaver that puts a pair of adorable eyes on any display. Hook it up to a phone running face detection, and watch as Blinky reacts to people walking by! Perfect for:

- Your work desk setup
- Shop windows
- Office spaces
- Smart mirror projects
- Anywhere that needs a bit more personality!

## Quick Start

1. First, make sure you have Node.js >=18 installed
2. Clone this repo
3. Install openssl if you haven't already
4. Generate a self-signed certificate:
```bash
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout certs/server.key -out certs/server.cert
```
Fill in the prompts (this is an example, fill in your own data):
```
Country Name: NL
State or Province Name: NL
Locality Name: NL
Organization Name: blinky
Organizational Unit: blinky
Common Name: Matthias Lubbertsen
Email: (can be skipped)
```
5. Install dependencies:
```bash
npm install
```
6. Start the server:
```bash
npm start
```

## Usage

1. Open https://YOUR_IP:8080 _(ip can be found in terminal)_ in Chrome on a computer or laptop (for bigger screen). Other browsers have not been tested yet, see GitHub issues for browser compatibility updates.
   - You'll get a security warning (self-signed cert)
   - Click "More info/Details" then "Continue to unsafe site"
2. On your phone (or another device), open https://YOUR_IP:8080/camera _(ip can be found in terminal)_

---
<img src="docs/assets/phone.jpg" alt="Phone Camera View" width="250" />

> [!NOTE]
> This face is blurred, but its not in the real app.
---
   - You'll get a security warning (because of the self-signed cert)
   - Click "More info/Details" then "Continue to unsafe site"
   - Accept the camera permission
   - Click "Start Detection"
3. Watch Blinky react when faces are detected!

### Files in public/
- `index.html` - The main Blinky application
- `phone.html` - The camera app for face detection
- `just_blink.html` - A simplified version with only the blinking animation
- `test_counter.html` - Test file for testing if the face detection counter works
- `working_version_with_local_camera.html` - Version using local camera but not synced
- `face-api.min.js` - Face detection library

## ⚠️ Privacy Note

Currently, Blinky doesn't implement face anonymization. If you plan to use this in a public space, consider:
- Adding face anonymization (also make Pull Request! This app needs that!) 
- THIS PROJECT DOES NOT FOLLOW LOCAL PRIVACY LAWS (GDPR/AVG)

I'm not responsible for any data collected/published using this software.

## Publishing/Credits

If you use or modify Blinky, you must credit Matthias Lubbertsen by linking to either:
- https://github.com/MatthiasLubbertsen
- https://matthias.is-a.dev

## License

MIT License + Credits clause - see [LICENSE.md](LICENSE.md)

---

## Credits

- Face detection powered by [face-api.js](https://github.com/justadudewhohacks/face-api.js) by @justadudewhohacks