# IPTV Token Logger

## Overview

This project is a web-based tool designed to activate IPTV subscriptions using JWT (JSON Web Tokens). It provides a simple interface for users to input their access tokens and perform subscription activation through API calls to an IPTV service server.

## Features

- **JWT Validation**: Validates the format of the input JWT token before processing.
- **Token Decoding**: Decodes the JWT payload to extract necessary information like codes and download links.
- **API Integration**: Makes secure HTTP requests to the IPTV server endpoints:
  - `GET /v1/codes` to retrieve activation codes
  - `POST /v1/subscriptions` to activate the subscription
- **User-Friendly Interface**: Clean, responsive UI with loading indicators and error handling.
- **Security Considerations**: Includes proper headers and handles rate limiting.

## How It Works

1. User enters a valid JWT access token in the input field.
2. Upon clicking "Activate", the tool:
   - Validates the JWT format
   - Sends a GET request to fetch codes using the token
   - Decodes the response to extract the activation code and download link
   - Sends a POST request to activate the subscription with the retrieved data
3. Displays the result, including success confirmation, code, and download link.

## Usage

1. Open `index.html` in a web browser (preferably served over HTTP to avoid mixed content issues).
2. Paste your JWT token into the input field.
3. Click the "Activate" button.
4. View the results in the displayed area.

## Technical Details

- **Frontend**: Pure HTML, CSS, and JavaScript (no frameworks required)
- **API Endpoints**: Communicates with `http://176.123.9.60:3000`
- **Authentication**: Uses Bearer token authentication
- **Error Handling**: Comprehensive error messages for various failure scenarios

## Disclaimer

This tool is for educational purposes only. Ensure you have proper authorization before using it with any services. The developers are not responsible for any misuse or violations of terms of service.
