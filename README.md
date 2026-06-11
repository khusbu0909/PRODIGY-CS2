# PRODIGY-CS2
## Task 02: Pixel Manipulation for Image Encryption

A simple Python-based image encryption tool that uses pixel manipulation to secure images. This tool allows users to encrypt and decrypt images by applying basic mathematical operations or swapping pixel values.

---

## Features
* *Image Encryption:* Encrypts an image by performing mathematical operations (like adding a key value or XORing) on each pixel.
* *Image Decryption:* Reverses the mathematical operation using the same key to restore the original image.
* *User-Friendly:* Simple command-line interface to input the image path and encryption key.

---

## Technologies Used
* *Python 3*
* *Pillow (PIL):* For image processing and pixel manipulation.

---

## How It Works
1. *Encryption:* The program loads the image, iterates through each pixel's RGB values, and applies a basic math operation (e.g., (pixel_value + key) % 256) or swaps values.
2. *Decryption:* The program takes the encrypted image and reverses the exact operation (e.g., (pixel_value - key) % 256) to get the original pixels back.

---

## Files in this Repository
* task2.py: The main Python script containing the encryption and decryption logic.
* encrypted_image.png: Output file generated after encryption.
* decrypted_image.png: Output file generated after decryption.
