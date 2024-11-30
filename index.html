<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>QR Code Scanner</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin: 0;
      padding: 0;
    }
    video {
      width: 100%;
      max-width: 600px;
      margin: 20px auto;
      border: 2px solid #333;
    }
    canvas {
      display: none;
    }
    button {
      background-color: #007BFF;
      color: white;
      border: none;
      padding: 10px 20px;
      font-size: 16px;
      cursor: pointer;
      margin: 10px;
    }
    button:disabled {
      background-color: #ccc;
      cursor: not-allowed;
    }
    #modal {
      display: none;
      position: fixed;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background-color: white;
      box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
      padding: 20px;
      border-radius: 10px;
      text-align: center;
      z-index: 1000;
    }
    #modal-overlay {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.5);
      z-index: 999;
    }
  </style>
</head>
<body>
  <h1>QR Code Scanner</h1>
  <video id="video" autoplay></video>
  <canvas id="canvas"></canvas>

  <div id="modal-overlay"></div>
  <div id="modal">
    <p id="qr-result">QR Code Value Here</p>
    <button id="close-modal">Close</button>
  </div>

  <script src="https://cdn.jsdelivr.net/npm/jsqr/dist/jsQR.min.js"></script>
  <script>
    const video = document.getElementById('video');
    const canvas = document.getElementById('canvas');
    const context = canvas.getContext('2d');
    const qrResult = document.getElementById('qr-result');
    const modal = document.getElementById('modal');
    const modalOverlay = document.getElementById('modal-overlay');
    const closeModal = document.getElementById('close-modal');
    const constraints = { video: { facingMode: "environment" } };

    let scanning = true;

    // Start camera and scan for QR codes
    async function startCamera() {
      try {
        const stream = await navigator.mediaDevices.getUserMedia(constraints);
        video.srcObject = stream;

        video.addEventListener('play', () => {
          scanQRCode();
        });
      } catch (error) {
        console.error('Error accessing the camera:', error);
        alert('Unable to access the camera. Please check your browser settings.');
      }
    }

    // Scan for QR codes continuously
    function scanQRCode() {
      if (!scanning) return;

      canvas.width = video.videoWidth;
      canvas.height = video.videoHeight;
      context.drawImage(video, 0, 0, canvas.width, canvas.height);

      const imageData = context.getImageData(0, 0, canvas.width, canvas.height);
      const code = jsQR(imageData.data, canvas.width, canvas.height);

      if (code) {
        scanning = false;
        qrResult.textContent = code.data;
        showModal();
      } else {
        requestAnimationFrame(scanQRCode);
      }
    }

    // Show the modal with the QR code value
    function showModal() {
      modal.style.display = 'block';
      modalOverlay.style.display = 'block';
    }

    // Close the modal and restart scanning
    closeModal.addEventListener('click', () => {
      modal.style.display = 'none';
      modalOverlay.style.display = 'none';
      scanning = true;
      scanQRCode();
    });

    // Initialize camera on page load
    window.addEventListener('load', startCamera);
  </script>
</body>
</html>
