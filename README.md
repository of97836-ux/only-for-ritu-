<!DOCTYPE html>
<html>
<head>
<style>
body{
  margin:0;
  padding:0;
  height:100vh;
  display:flex;
  justify-content:center;
  align-items:center;
  flex-direction:column;
  background: linear-gradient(45deg, #ff9a9e, #fad0c4);
  font-family: Arial, sans-serif;
  overflow:hidden;
}

img{
  width:250px;
  border-radius:20px;
  box-shadow:0 0 25px rgba(255,255,255,0.8);
  animation: zoomIn 3s infinite alternate;
}

#loveText{
  font-size:45px;
  margin-top:20px;
  color:white;
  text-align:center;
  animation: glow 1s infinite alternate;
}

@keyframes glow{
  from{
    text-shadow:0 0 10px white, 0 0 20px pink;
  }
  to{
    text-shadow:0 0 20px red, 0 0 40px white;
  }
}

@keyframes zoomIn{
  from{
    transform:scale(1);
  }
  to{
    transform:scale(1.1);
  }
}
</style>
</head>

<body>

<img src="img1.jpg.jpeg" alt="Love Image">

<h1 id="loveText"></h1>

<script>
let text = "I Love You ❤️";
let i = 0;

function typeLove(){
  if(i < text.length){
    document.getElementById("loveText").innerHTML += text.charAt(i);
    i++;
    setTimeout(typeLove, 200);
  }
}
typeLove();
</script>

</body>
</html>
