<!DOCTYPE html>
<html>
<head>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black">

  <style>
    video { width: 100%; background:#000; }
    button { padding: 15px; width: 100%; font-size: 18px; }
  </style>
</head>

<body>
  <h3>iPad Camera Working Page</h3>

  <video id="cam" autoplay playsinline muted></video><br><br>

  <button type="button" onclick="startCam()">Start Camera</button>

  <script>
    function startCam() {
      navigator.mediaDevices.getUserMedia({ video: true })
        .then(stream => cam.srcObject = stream)
        .catch(err => alert("Camera Error: " + err));
    }
  </script>

</body>
</html>
