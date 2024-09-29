# SIH 2024 Problem ID: 1674 - Tracing Drug Dealers on Telegram, Instagram, WhatsApp

## Overview

This project addresses a challenge presented by the National Crime Bureau (NCB) during the Smart India Hackathon (SIH) 2024. The goal is to trace and track drug dealers utilizing channels and bots on Telegram, Instagram, and WhatsApp. The solution leverages Natural Language Processing (NLP) and Blockchain technologies to analyze text messages and images for suspicious content related to drug transactions.

# NCB Suspicious Message Detection and IP Tracking System

This project is developed for **Smart India Hackathon (SIH) 2024**, Project ID: **1674**. The system detects suspicious messages related to drug trafficking and logs them into a simulated blockchain. It also extracts text from images using OCR and tracks IP addresses to show their locations on Google Maps.

## Table of Contents
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Example Output](#example-output)
- [Contributors](#contributors)

## Features
1. **NLP-based Suspicious Message Detection**: Detects drug-related terms in text messages.
2. **OCR Image Processing**: Extracts and analyzes text from images using OCR (Tesseract).
3. **Blockchain Logging**: Logs processed messages to a simulated blockchain with unique hash identifiers.
4. **IP Tracking**: Retrieves and displays the geographical location of IP addresses using Google Maps.
5. **Result Logging**: Saves processed results to a `result.txt` file.

## Project Structure
- `main.py`: The main file that orchestrates the message processing, importing other functionalities.
- `result_writer.py`: Writes the output to `result.txt` after analyzing messages and images.
- `ip_tracker.py`: Tracks IP addresses and shows their location on Google Maps using the `folium` library.
- `README.md`: Project documentation.

## Installation

### Prerequisites
- Python 3.x
- Install necessary Python packages:
  ```
  pip install spacy pytesseract Pillow folium
  ```

### Additional Setup
- Download and install Tesseract OCR: [Tesseract Installation](https://github.com/tesseract-ocr/tesseract).
- Make sure to set the path to Tesseract in the `pytesseract.pytesseract.tesseract_cmd` line in the code.

### Running the project
Clone the repository or download the files and navigate to the project directory:

```
git clone https://github.com/your-repo-link.git
cd NCB-2
```

Run the `main.py` file:

```
python main.py
```

## Usage
1. **Message Processing**:
   - The system can process both text messages and images to detect suspicious content.
   - Text messages and extracted image text are analyzed for drug-related terms using NLP.
   - IP addresses of the message sender and receiver are logged and tracked.

2. **Blockchain Logging**:
   - Every processed message (either text or image) is logged to a simulated blockchain.

3. **Result Logging**:
   - The processed results, including suspicious message detection, are saved to a `result.txt` file.

4. **IP Tracking**:
   - The IP addresses are tracked and their locations are displayed on a map using Google Maps through `folium`.

## Example Output

1. **Blockchain Log**:
   ```
   ALERT: Suspicious message detected! - ['grams', 'shipment']
   Processed Message: Need 100 grams for shipment tomorrow
   Logged to blockchain: {'block_id': '982b26695d69c9f215c1e28ca3ffa211894369021b53bf913988e485ce23398b', 
   'data': {'sender_ip': '192.168.1.25', 'receiver_ip': '203.0.113.78', 'analysis': {'message': 'Need 100 grams for shipment tomorrow', 
   'keywords_detected': ['grams', 'shipment'], 'suspicion_level': 'high', 'flag_reason': 'Drug-related terms detected'}, 
   'timestamp': '2024-09-26T12:13:44.260581'}}
   ```

2. **Result File (`result.txt`)**:
   ```
   Processed Message: Need 100 grams for shipment tomorrow
   Keywords Detected: grams, shipment
   Suspicion Level: high
   Flag Reason: Drug-related terms detected
   Sender IP: 192.168.1.25
   Receiver IP: 203.0.113.78
   Timestamp: 2024-09-26T12:13:44.260581
   ```

3. **Map Output**:
   After running the program, a map will open displaying the locations of the IP addresses.

## Contributors
- Project developed by InsightOps we are a Team of 6 people.
- *P.Saifullah khan*
- *B.Gopi Kalyan*
- *T.Bhanu*
- *P.Sumanth*
- *P.Dany Arshith*
- *Sk.Nousheen*
- For **Smart India Hackathon 2024**, ID **1674**.
```

## Conclusion
This project presents an innovative solution for monitoring and detecting drug-related activities on social media platforms using advanced NLP and Blockchain technologies.
Future enhancements may include expanding the range of monitored platforms and integrating real-time alert systems for law enforcement agencies.

This `README.md` provides a detailed guide on the project, its structure, how to install it, and how to run it.
