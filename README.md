<!DOCTYPE html>
<html>
<head>
<meta name=viewport content="width=device-width,initial-scale=1">
<meta charset="utf-8"/>
<script src="https://cdn.geogebra.org/apps/deployggb.js"></script>

<style type="text/css">
body {
    background-image: url("20200427_085350.jpg");
}
</style>
</head>

<h1>Trabajo con applet </h1>

<p> Esta es la primeraa funcion del ejercicio de poligono de no se quien chingados</p>
	
<div id="ggbApplet"></div>
	

<script>
var parameters = {
"id": "ggbApplet",
"width":1000,
"height":500,
"showMenuBar":true,
"showAlgebraInput":true,
"showToolBar":true,
"customToolBar":"0 73 62 | 1 501 67 , 5 19 , 72 75 76 | 2 15 45 , 18 65 , 7 37 | 4 3 8 9 , 13 44 , 58 , 47 | 16 51 64 , 70 | 10 34 53 11 , 24  20 22 , 21 23 | 55 56 57 , 12 | 36 46 , 38 49  50 , 71  14  68 | 30 29 54 32 31 33 | 25 17 26 60 52 61 | 40 41 42 , 27 28 35 , 6",
"showToolBarHelp":true,
"showResetIcon":false,
"enableLabelDrags":false,
"enableShiftDragZoom":true,
"enableRightClick":false,
"errorDialogsActive":false,
"useBrowserForJS":false,
"allowStyleBar":false,
"preventFocus":false,
"showZoomButtons":true,
"capturingThreshold":3,
// add code here to run when the applet starts
"appletOnLoad":function(api){ /* api.evalCommand('Segment((1,2),(3,4))');*/ },
"showFullscreenButton":true,
"scale":1,
"disableAutoScale":false,
"allowUpscale":false,
"clickToLoad":false,
"appName":"classic",
"showSuggestionButtons":true,
"buttonRounding":0.7,
"buttonShadows":false,
"language":"es",
// use this instead of ggbBase64 to load a material from geogebra.org
// "material_id":"RHYH3UQ8",
// use this instead of ggbBase64 to load a .ggb file
// "filename":"myfile.ggb",
"ggbBase64":"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",
};
// is3D=is 3D applet using 3D view, AV=Algebra View, SV=Spreadsheet View, CV=CAS View, EV2=Graphics View 2, CP=Construction Protocol, PC=Probability Calculator DA=Data Analysis, FI=Function Inspector, macro=Macros
var views = {'is3D': 1,'AV': 1,'SV': 0,'CV': 0,'EV2': 0,'CP': 1,'PC': 0,'DA': 0,'FI': 0,'macro': 0};
var applet = new GGBApplet(parameters, '5.0', views);
window.onload = function() {applet.inject('ggbApplet')};
applet.setPreviewImage('data:image/gif;base64,R0lGODlhAQABAAAAADs=','https://www.geogebra.org/images/GeoGebra_loading.png','https://www.geogebra.org/images/applet_play.png');
</script>
	
</body>
</html>

