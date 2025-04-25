# Web NFC Reader with Tailwind UI

## Overview
This above demonstrates how to use the Web NFC API to read encrypted NFC tag data, decrypt it using AES, and send a response ("Scan complete ✅") back to the tag. It includes a clean UI built with Tailwind CSS.

## Features
- Read NFC tags using Web NFC API
- Decrypt encrypted Base64 messages using AES (ECB mode)
- Send acknowledgment back to the tag
- Tailwind-styled UI with a responsive design

## Files
- `index.html`: Main HTML file containing UI, JavaScript, and Tailwind integration

## How It Works

### 1. UI Elements
- A button to start scanning (`Start NFC Scan`)
- A styled output box that logs scan status, decrypted data, and acknowledgments

### 2. AES Decryption Function
Uses CryptoJS to decrypt base64-encoded messages from the tag using a pre-shared AES key (`1234567890123456`).

### 3. Web NFC Scan Logic
- Checks if `NDEFReader` is supported
- Starts scanning on button click
- On reading an NFC tag, it:
  - Decodes the message
  - Decrypts and logs the payload
  - Sends a response message back to the tag

## Requirements
- A device with NFC support (typically Android + Chrome)
- Real NFC tags or an HCE-based tag emulator on Android

## Limitations
- Web NFC API does not support tag emulation (only reading/writing)
- Must be served over HTTPS or localhost

## Credits
- Tailwind CSS CDN for styling
- CryptoJS CDN for AES decryption

## License
MIT License (Free to use)