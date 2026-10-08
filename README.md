[face_sample.html](https://github.com/user-attachments/files/33194215/face_sample.html)
<!DOCTYPE html>
<html>
<head>

  <meta charset="UTF-8">

  <meta name="viewport"
        content="width=device-width, initial-scale=1.0">

  <!-- A-Frame -->
  <script src="https://aframe.io/releases/1.6.0/aframe.min.js"></script>

  <!-- MindAR Face Tracking -->
  <script src="https://cdn.jsdelivr.net/npm/mind-ar@1.2.5/dist/mindar-face-aframe.prod.js"></script>

  <style>
    html, body {
      margin: 0;
      width: 100%;
      height: 100%;
      overflow: hidden;
    }

    a-scene {
      width: 100%;
      height: 100%;
    }
  </style>

</head>

<body>

<a-scene
  mindar-face
  embedded
  color-space="sRGB"
  renderer="colorManagement: true"
  vr-mode-ui="enabled: false"
  device-orientation-permission-ui="enabled: false">

  <!-- ========================= -->
  <!-- โหลดโมเดล -->
  <!-- ========================= -->

  <a-assets>

    <!-- แว่น -->
    <a-asset-item
      id="balencigaGlass"
      src="https://cdn.jsdelivr.net/gh/ketareiei-design/-AR-Face-Mesh-Texture@main/balenciga%20glass.glb">
    </a-asset-item>

    <!-- หมวก Cowboy -->
    <a-asset-item
      id="cowboyHat"
      src="https://cdn.jsdelivr.net/gh/ketareiei-design/-AR-Face-Mesh-Texture@main/cowboy_hat.glb">
    </a-asset-item>

    <!-- Head Occluder -->
    <a-asset-item
      id="headModel"
      src="https://cdn.jsdelivr.net/gh/hiukim/mind-ar-js@1.2.5/examples/face-tracking/assets/sparkar/headOccluder.glb">
    </a-asset-item>

  </a-assets>


  <!-- ========================= -->
  <!-- กล้อง -->
  <!-- ========================= -->

  <a-camera
    active="false"
    position="0 0 0">
  </a-camera>


  <!-- ========================= -->
  <!-- แว่น -->
  <!-- Anchor 168 -->
  <!-- ========================= -->

  <a-entity mindar-face-target="anchorIndex: 168">

    <a-gltf-model
      src="#balencigaGlass"
      position="0 0 0"
      rotation="0 0 0"
      scale="0.2 0.2 0.2">
    </a-gltf-model>

  </a-entity>


  <!-- ========================= -->
  <!-- หมวก Cowboy -->
  <!-- Anchor 151 -->
  <!-- ========================= -->

  <a-entity mindar-face-target="anchorIndex: 151">

    <a-gltf-model
      src="#cowboyHat"
      position="0 0 0"
      rotation="0 0 0"
      scale="0.2 0.2 0.2">
    </a-gltf-model>

  </a-entity>


</a-scene>

</body>
</html>
