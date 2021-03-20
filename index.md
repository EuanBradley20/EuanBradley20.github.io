<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
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
  background: #272838;
  color: #f1f1f1;
}

.content{
  padding: 16px;
}

.sticky{
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
}

.sticky + .content {
  padding-top: 102px;
}

</style>
</head>
<body style="background-color: #A7B0CA;">

<div class="row">
  <div class="header" id="myHeader">
    <h1>The Quizzicle</h1>
  </div>
  <div class="column" style="background-color: #2B2D42;">
    <h2 style="color:wheat">Column 1</h2>
    <p style="color:wheat">Some text..</p>
  </div>
  <div class="column" style="background-color:#8D99AE;">
    <h2>Column 2</h2>
    <p>Some text..</p>
  </div>
  <div class="column2" style="background-color:#EDF2F4;">
    <h2>Column 2</h2>
    <p>Some text..</p>
    <table border="1" style="width:100%">
      <tr>
        <th style="width:50%"> <b>Team Name</b> </th>
        <th style="width:50%"> <b>Win Total</b> </th>
      </tr>
      <tr>
        <td style="width:50%"> Placeholder</td>
        <td style="width:50%"> Placeholder</td>
      </tr>
    </table>
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
