# Best_Responsive_Page 

<html>

	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1">
		<title>Mondrain Layout</title>
		<link href="images/favicon.ico" rel="icon" type="image/x-icon" />
		<link rel="stylesheet" href="mondrian.css">
	</head>
    
	<body> 
	     <!-- The brown column is Centerd the div properties vertical and horizontal --> 
		<div class="wide-col SaddleBrown center-vertical center-horizontal">  
			<img src="images/cubo_grande.png" class="contain-image"> 
		</div>   
		<div class="narrow-col"> 
		    <div class="box BlueViolet"></div> 
			<div class="box DarkCyan"></div>  			
			<div class="box FireBrick"></div> 
		</div>
	</body>
	
</html> 


body {
	width: 100%;
	height: 100%;
	margin: 0; 
	display: flex;
}

.wide-col {  
	display: flex;
	width: 65%; 
	height:100%;
}

.narrow-col { 
    display: block;
	height: 100%;
	width: 35%; 
}

.box {
	/* The calc function is used for calculation. Its helpful for dividing different properties */
	height: calc(100% / 3);
	width: 100%; 
} 



.blue {background-color: #0D11A8; }
.red {background-color: #F50F0F;}
.yellow {background-color: #FAE317;} 
.DarkCyan {background-color: #008B8B;}
.FireBrick {background-color: #B22222;} 
.SaddleBrown {background-color: #8B4513;} 
.BlueViolet {background-color: #8A2BE2;}

/* https://philipwalton.github.io/solved-by-flexbox/demos/vertical-centering/ */
/* If you're using 'display: flex' this class can be used to easily center horizontally! */
.center-horizontal {
	align-items: center;	
}

/* If you're using 'display: flex' this class can be used to easily center vertically! */
.center-vertical {
	justify-content: center;
}

/* Keep your image from overflowing it's parent DIV */
.contain-image {
	max-height: 75%;
	max-width: 75%; 

} 



@media only screen and (max-width: 1000px) {
	.contain-image {
		height: auto;
	}
    body { 
	  display: block; 
	}
	
	.wide-col {  
	 width: 100%; 
	 height:65%;
    }

   .narrow-col { 
	 height: 35%;
	 width: 100%; 
	 display: flex;
    } 
	
    .box {
	  height: 100%;
	  width: 50%; 
    } 
    	
	  
		 
}


@media only screen and (max-width: 700px) {
	.contain-image {
		height: auto;
	}
    body { 
	  display: block; 
	}
	
   .narrow-col { 
	 height: 35%;
	 width: 100%; 
	 display: block;
    } 
	
    .box {
	  height: 100%;
	  width: 100%; 
    } 
    	
	  
		 
}
