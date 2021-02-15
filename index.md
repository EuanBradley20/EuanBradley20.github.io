<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1">
<style>
* {
  box-sizing: border-box;
}
h1 {text-align: center;}
h2 {text-align: center;}

.column {
  float: left;
  width: 50%;
  padding: 10px;
  height: 500px;
}

.column2 {
  float: left;
  width: 100%;
  padding: 10px;
  height: 400px;
}

.row:after {
  content: "";
  display: table;
  clear: both;
}

body {
    font-family: Garamond, serif;
}

.header {
  padding: 10px 16px;
  background: rgb(104, 15, 92);
  color: #f1f1f1;
}

.content{
  padding: 16px;
}

.sticky{
  position: fixed;
  top: 0;
  width: 45%
}

.sticky + .content {
  padding-top: 102px;
}

</style>
</head>
<body style="background-color: #292930">

<div class="header" id="myHeader">
    <h1>The Quizzicle</h1>
</div>

<div class="row">
  <div class="column" style="background-color: #441166;">
    <h2 style="color:wheat">Column 1</h2>
    <p style="color:wheat">Some text..</p>
  </div>
  <div class="column" style="background-color:#28472a;">
    <h2>Column 2</h2>
    <p>Some text..</p>
  </div>
  <div class="column2" style="background-color:#b6b6b6;">
    <h2>Column 2</h2>
    <p>Some text..</p>
  </div>
</div>

<script>
  window.onscroll = function() {myFunction()};

  var header = document.getElementById("myHeader");
  var sticky = header.offsetTop;

  function myFunction() {
    if (window.pageYOffset > sticky){
      header.classList.add("sticky");
    } else{
      header.classList.remove("sticky");
    }
  }
</script>

</body>
</html>
