# Chromium---Browser-Technology
Chromium-&amp;-Browser-Technology


# How Web Browsers Function
	https://www.youtube.com/watch?v=z0HN-fG6oT4

	Renderer Engine - HTML/CSS/xml other files to display,audio/video/svg/image
		edge			    -	Blink now (earlier EdheHTML engine)
		chrome/opera	-	Blink
		firefox 		  - gecko
		safari 			  -	webkit
		
	Browser Engine 	-  communicate user input action to renderer engine/ or external comm to network service
	  EdgeHTML is a proprietary browser engine from Microsoft,
    now Edge as a Chromium-based browser,[2][3] using the Blink engine;
    
	JS interpretor
		edge	-	Chakra
		chrome	-	V8
		firefox - 	spider monkey

	Data Storage
		Cookies		-		
		Local Data	-


	1.	network layer -> html/css/xml all docs -> rendering engine
	2.	rendering engine read html/css file and construct DOM Tree, html and css style are part of CSSOM Node
			https://developers.google.com/web/fundamentals/performance/critical-rendering-path/constructing-the-object-model
			Bytes → characters → tokens → nodes → object model.
			HTML markup is transformed into a Document Object Model (DOM); CSS markup is transformed into a CSS Object Model (CSSOM).
			DOM and CSSOM are independent data structures.
  3. combine DOM and CSSOM new tree chreated Render Tree
  4. after this Painting Phase started(Rasterise) (open Canvas -> put View port -> ) Layout is put in their coordinates , 
    then Render Tree is parsed by UI Backend Layer.
      Run Layout on  Render tree to compute Geometry of each NODE.
      Paint Each Node to Screen
  5 . Once PArsing of document is done, Browser mark the Page as "Interactive" . 
  
# IE vs EDGE
  https://en.wikipedia.org/wiki/Microsoft_Edge
  Unlike Internet Explorer, Edge does not support the legacy ActiveX and BHO technologies( Browser Helper Objects).
  
  EdgeHTML
    EdgeHTML was the proprietary layout engine originally developed for Edge. 
    EdgeHTML was written in C++
    EdgeHTML was meant to be fully compatible with the WebKit layout engine used by Safari, Chrome, and other browsers.
    As of September 2019, Edge 17 had scored 492/555 on HTML5test, whereas Firefox 59 scored 491/555, Firefox 69 scored 513/555 and Chrome 66 scored 528/555.[36]
 
# Browser engine
  https://en.wikipedia.org/wiki/Browser_engine
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
