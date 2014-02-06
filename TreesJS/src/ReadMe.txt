2. Feb 6 improved the drawing of the lines by fixing their height and letting their
	width scale
	stopped the justification wrapping by substituting non-breaking space for space
	stopped autoscroll to center (not good when selecting out wide) by redrawing only
	rather than recalculating everything
	experimented with resizable header for table, but not using it just yet
	experimented with jquery possibly to replace gwt celltable

1.	Jan 30 2014 diagonals not drawing well, and columns should resize

	at present being drawn by
	
	<img src="images/rightDiag.png" style="width:100%; height:100%;">
	
	scaled to fit the cell. Drawn in TTreeCustomCell.java
	
	The solution to this might be to use a horizontal rule then css transform it
	
	HTML Code:
<!DOCTYPE html>
<html>
<head>
<style type="text/css">
hr {
transform:rotate(5deg);
-ms-transform:rotate(5deg); 
-moz-transform:rotate(5deg); 
-webkit-transform:rotate(5deg);
-o-transform:rotate(5deg);
}
</style>
</head>
<body>

<hr></hr>

</body>
</html>