# Blinky 👀

A delightful screensaver pet with animated eyes that follows faces using your phone's camera!

![Blinky Demo](docs/assets/demo.gif)
*[Add a GIF of Blinky in action]*

![Phone Camera View](docs/assets/phone.png)
*[Add a screenshot of the phone camera interface]*

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
openssl req -x509 -nodes -days 30 -newkey rsa:2048 -keyout certs/server.key -out certs/server.cert
```
Fill in the prompts (this is an example, fill in your own data):
```
Country Name: NL
State/Province: NL
Locality: NL
Organization Name: blinky
Organizational Unit: blinky
Common Name: Matthias Lubbertsen
Email: (can skip)
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

1. Open https://YOUR_IP:8080 (ip can be found in terminal) in your browser
   - You'll get a security warning (self-signed cert)
   - Click "More info/Details" then "Continue to unsafe site"
2. On your phone, open https://YOUR_IP:8080/camera
   - You'll get a security warning (self-signed cert)
   - Click "More info/Details" then "Continue to unsafe site"
   - Accept the camera permission
   - Click "Start Detection"
3. Watch Blinky react when faces are detected!

## ⚠️ Privacy Note

Currently, Blinky doesn't implement face anonymization. If you plan to use this in a public space, consider:
- Adding face anonimization (also make Pull Reqest! This app needs that!) 
- Getting proper consent
- THIS PROJECT DOES NOT FOLLOWS LOCAL PRIVACY LAWS (GDPR/AVG)

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