# steganography

## 📌 Overview
This repository contains the source code and graphical user interface (GUI) for an **Audio Steganography** tool. Steganography is the practice of concealing a secret message within an ordinary, non-secret file or message to avoid detection. 

In this project, a secret audio message is securely embedded inside a larger, innocent-sounding "cover" audio file using **Spread Spectrum** techniques. This method ensures that the hidden message is distributed across the frequency spectrum of the cover signal, making the embedded data highly robust against noise, tampering, and detection by human hearing.

## 🚀 Key Features
* **Graphical User Interface (GUI):** A user-friendly dashboard that allows for easy selection of cover and message files, execution of the embedding process, and extraction of the hidden data.
* **Spread Spectrum Encoding:** Provides high security and robustness compared to simple Least Significant Bit (LSB) methods.
* **Signal Verification:** Includes waveform plotting tools to visually verify that the cover signal is not significantly distorted by the embedding process.

## ⚙️ How It Works
1. **Embedding Process:** The algorithm reads the digital samples of the cover audio and the secret message audio. Using a spread spectrum key/sequence, the secret message is modulated and added to the cover signal, producing the `stego_audio.wav`.
2. **Transmission:** The stego audio can be safely transmitted over standard communication channels. To a casual listener, it sounds identical to the original cover file.
3. **Extraction Process:** The receiver uses the extraction algorithm (and the corresponding key/sequence) to isolate the spread spectrum signal from the stego audio, successfully reconstructing the `extracted_message.wav`.

