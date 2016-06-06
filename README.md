# I-am-trying-so-hard
Trying to create something for work...
<html>
<head>
<script src="./src/signature_pad.js"></script>
<style>
	body {background-color: white;}
h1   {color:black;}
p    {color:green;}
</style>

<div class="CORE">
    <img src="https://corebio.ucsd.edu/images/CORELogoBlack.png" />
</div>

<div class="h1">
<h1>PLEASE SIGN HERE</h1>
</div>

</head>


<body>

<canvas style="width: 1000px; height:300px; border: 2px solid;"></canvas>

<div style="width:50px; height:25px">
     <button type="button" onclick="signaturePad.clear()">Clear</button>
</div>

<div style="width:50px; height:25px">
     <input type="button" value="Save" onclick="window.open(signaturePad.toDataURL())">
</div>

<p>THANK YOU FOR USING BIO CORE SERVICES</p>

<style>
    canvas {
    padding-left: 0;
    padding-right: 0;
    margin-left: auto;
    margin-right: auto;
    display: block;
    width: 800px;
    margin-bottom: 0;
    }

    .CORE {
        margin-left: 41%;
    }

    .h1 {
        height: 50px;
        width: 100%;
        margin-left: 41%;
    }
</style>
<!-- What do you think you are doing? -->
</body>

<script>

var canvas = document.querySelector("canvas");
var signaturePad = new SignaturePad(canvas,{
	minWidth: 1,
	maxWidth: 1,
	penColor: "rgb(128, 128, 128)"

});

function resizeCanvas() {
    var ratio =  Math.max(window.devicePixelRatio || 1, 1);
    canvas.width = canvas.offsetWidth * ratio;
    canvas.height = canvas.offsetHeight * ratio;
    canvas.getContext("2d").scale(ratio, ratio);
    signaturePad.clear(); // otherwise isEmpty() might return incorrect value
}



window.addEventListener("resize", resizeCanvas);
resizeCanvas();

</script>

</html>
