# OpenCV QR Code Scanner OpenCV

This project provides a python-based QR code scanner that uses OpenCV and Pyzbar libraries to capture QR codes via webcam, detect URLs, and automatically open them in a new browser tab. It’s designed for seamless integration with Chrome, making it ideal for quick QR code testing and website redirection.

## Project Overview

This project leverages **OpenCV** for image capture and **Pyzbar** for QR code decoding. The scanner reads frames from the webcam in real-time, detects QR codes, and checks if they contain a URL. Once a URL is detected, it stops the camera feed and opens the link in a new tab in Chrome, providing an automated and efficient solution for QR code redirection.

## Features

- Real-time QR code scanning via the webcam.
- Automatic detection and decoding of QR codes.
- Opens detected URLs in a new Chrome tab automatically.
- Runs seamlessly in a Jupyter Notebook environment.
- Simple, modular code structure for easy customization and expansion.

## Prerequisites

To run this notebook, you'll need:

- Python 3.x
- Jupyter Notebook (or JupyterLab)
- Google Chrome (already set as the default browser)
  
Install the required libraries:

```bash
pip install opencv-python pyzbar
```

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/ahmdmohamedd/QR-Code-Scanner-OpenCV.git
   cd QR-Code-Scanner-OpenCV
   ```

2. Open the Jupyter Notebook in your browser:

   ```bash
   jupyter notebook QR_Code_Scanner_OpenCV.ipynb
   ```

3. Run the cells sequentially. The notebook is structured to guide you step-by-step through the QR code scanner setup.

4. Once the system detects a QR code with a URL, it will automatically open the URL in a new tab in Chrome, and the camera feed will stop.

### How It Works

The notebook is divided into the following main steps:

1. **Install Required Libraries**: Installs OpenCV and Pyzbar.
2. **Import Required Libraries**: Imports OpenCV, Pyzbar, web browser control, and other necessary modules.
3. **Initialize Camera**: Sets up the webcam for frame capture.
4. **QR Code Detection with URL Opening**: Detects QR codes in each frame, opens the URL in Chrome, and stops further processing.
5. **Run QR Code Scanner**: Starts the main loop for capturing frames, processing QR codes, and stopping once a URL is opened.

### Example QR Code

You can test the system with the following sample QR code:

![QR Code Example](./test_qr_code.png)  
This QR code links to "[https://example.com](https://idemia-mobile-id.com/testqr-success)" this is a website specifically for testing qr code readers.

## Customization

The notebook can be easily customized for different use cases:

- **Camera Source**: Modify the `initialize_camera()` function to use a different camera source.
- **Display Settings**: Adjust the `cv2.imshow()` settings to change the display window's size or position.
- **Custom Actions**: Replace the `webbrowser.open_new_tab(qr_data)` command to perform different actions based on the decoded QR code data.

## Troubleshooting

- **Webcam Issues**: Ensure no other applications are using the webcam when running the notebook.
- **URL Not Opening**: Confirm that Chrome is set as the default browser.
- **Dependencies**: If the notebook does not recognize OpenCV or Pyzbar, verify the installations and Python path.

## Contributing

Feel free to fork this repository, submit pull requests, or suggest new features! Contributions are always welcome.
