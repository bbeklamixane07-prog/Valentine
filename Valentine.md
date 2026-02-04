# Valentine  
<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8">  
  <meta name="viewport" content="width=device-width, initial-scale=1.0">  
  <title>Be My Valentine ❤️</title>  
  <style>  
    body {  
      font-family: 'Poppins', sans-serif;  
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      height: 100vh;  
      margin: 0;  
      text-align: center;  
    }  
  
    .box {  
      background: white;  
      padding: 30px;  
      border-radius: 15px;  
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);  
      max-width: 350px;  
      width: 90%;  
    }  
  
    h1 {  
      margin-bottom: 20px;  
      color: #ff4d6d;  
    }  
  
    button {  
      border: none;  
      padding: 12px 25px;  
      font-size: 16px;  
      border-radius: 8px;  
      cursor: pointer;  
      margin: 10px;  
      transition: all 0.3s ease;  
    }  
  
    #yesBtn {  
      background: #ff4d6d;  
      color: white;  
      font-size: 18px;  
    }  
  
    #noBtn {  
      background: #aaa;  
      color: black;  
    }  
  
    #message {  
      margin-top: 20px;  
      font-size: 18px;  
      color: #ff4d6d;  
      font-weight: bold;  
    }  
  </style>  
</head>  
<body>  
  
  <div class="box">  
    <h1>Will you be my Valentine? 💖</h1>  
  
    <button id="yesBtn" onclick="yesClicked()">Yes ❤️</button>  
    <button id="noBtn" onclick="noClicked()">No 😢</button>  
  
    <div id="message"></div>  
  </div>  
  
  <script>  
    let yesSize = 18;  
  
    function noClicked() {  
      yesSize += 8;  
      const yesBtn = document.getElementById("yesBtn");  
      yesBtn.style.fontSize = yesSize + "px";  
      yesBtn.style.padding = (12 + yesSize/3) + "px " + (25 + yesSize/2) + "px";  
  
      if (yesSize > 60) {  
        document.getElementById("noBtn").style.display = "none";  
      }  
    }  
  
    function yesClicked() {  
      document.querySelector(".box").innerHTML =   
        "<h1>Yayyyy!! 😍❤️</h1>" +  
        "<p id='message'>Now you are officially my Valentine 💕<br>I can’t wait to make beautiful memories with you 😘</p>";  
    }  
  </script>  
  
</body>  
</html>  
