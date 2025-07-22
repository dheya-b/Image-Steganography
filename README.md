# 🔐 Advanced Image Steganography using Deep Learning and Cryptography

This project showcases a **secure image steganography system** that embeds encrypted and authenticated secret messages into images using **bit-plane LSB manipulation**. It also evaluates the quality of stego images and assesses resistance to steganalysis.

## 🚀 Features

- **AES Encryption**: Ensures message confidentiality.
- **HMAC Authentication**: Validates message integrity and authenticity.
- **Bit-Plane LSB Embedding**: Steganographic technique that embeds data in least significant bits of an image.
- **Image Quality Metrics**: Calculates PSNR, MSE, and SSIM to evaluate distortion.
- **RS Steganalysis**: Detects presence of hidden data by analyzing pixel patterns.

## 📁 Project Structure

- `image_steganography_code.ipynb`: Main notebook implementing the pipeline.
- `cover_image.png`: Image used to hide data (user-supplied).
- `secret.txt`: Text file containing secret message (user-supplied).
- `stego_image.png`: Output image containing the hidden message.

## 🧠 Workflow Overview

1. **Message Encryption**
   - Encrypts the input message using AES-CBC with a user-defined key.
   - Generates HMAC for message integrity.

2. **Embedding in Image**
   - Converts encrypted message into bits.
   - Embeds these bits in the least significant bits of selected bit-planes in the cover image.

3. **Stego Image Evaluation**
   - Measures PSNR, MSE, and SSIM between cover and stego images.
   - Performs RS analysis for detectability.

4. **Extraction & Decryption**
   - Recovers message bits from the stego image.
   - Validates HMAC and decrypts message.

## 📊 Metrics Used

| Metric | Description |
|--------|-------------|
| PSNR   | Peak Signal-to-Noise Ratio |
| MSE    | Mean Squared Error |
| SSIM   | Structural Similarity Index |
| RS Analysis | Steganalysis technique for LSB detection |

## 🛠️ Requirements

- Python 3.7+
- NumPy
- OpenCV (`cv2`)
- Matplotlib
- Cryptography (`cryptography` module)
- scikit-image

Install dependencies:
```bash
pip install -r requirements.txt
```

## ✅ Usage

1. Load the Jupyter Notebook:
```bash
jupyter notebook image_steganography_code.ipynb
```

2. Upload your:
   - Cover image
   - Secret message file

3. Follow the notebook cells to:
   - Encrypt → Embed → Generate stego image
   - Extract → Decrypt → Validate message

## 🔐 Security Notes

- AES 256-bit encryption with CBC mode ensures message confidentiality.
- HMAC-SHA256 provides strong integrity checks.
- Bit-plane selection can be randomized for added security.

## 🧪 Future Improvements

- Deep Learning-based steganographic embedding.
- Adaptive embedding based on image complexity.
- Use of GANs to generate more secure stego images.

## 🧑‍💻 Author

**Dheya Badrinath**  
Feel free to connect via [LinkedIn](#) or email.

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
