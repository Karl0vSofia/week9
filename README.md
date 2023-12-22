<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>MindAR with A-frame</title>
  <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/mindarjs"></script>
</head>
<body>
  
  <a-scene>
    
    <a-marker preset="custom" type="pattern" url="../SonyaIT/Apple_Store_logo.svg">
     
      <a-video src="https://static.videezy.com/system/resources/previews/000/042/042/original/Ramdom_Lines_x264.mp4" width="2" height="1.5" position="0 0.75 0"></a-video>
    </a-marker>

    
    <a-marker preset="custom" type="pattern" url="../SonyaIT/356952183.webp">
      
      <a-entity
        gltf-model="../SonyaIT/yellow-brick-3d-model/yellow_brick_4k.gltf"
        scale="0.02 0.02 0.02"
        rotation="0 180 0"
        position="0 0 0">
      </a-entity>
    </a-marker>

   
    <a-entity camera position="0 3 10"></a-entity>
  </a-scene>
  
  
  <script>
    document.addEventListener("DOMContentLoaded", function () {
      // Ініціалізація MindAR
      MindAR.initialize();
      
      // Виявлення маркерів
      MindAR.trackMarkers();
    });
  </script>
</body>
</html>
