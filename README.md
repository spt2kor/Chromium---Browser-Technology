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
  Besides "browser engine", two other terms are in common use regarding related concepts: "layout engine" and "rendering engine".[1][2][3] In theory, layout and rendering (or "painting") could be handled by separate engines. In practice, however, they are tightly coupled and rarely considered separately.
  
  JS Engine and Browser Engine
  the implementation of JS engines is decoupled from browser engines. In a web browser, the two engines work in concert via the shared DOM data structure.
  
  Browser engines are used in other types of programs besides web browsers. Email clients need them to display HTML email. The Electron framework, which is powered by the two engines of the Google Chrome browser, has been used to create many applications.
  
 WEBKIT 
  Google originally used WebKit for its Chrome browser but eventually forked it to create the Blink engine.[6] All Chromium-based browsers use Blink, as do applications built with CEF, Electron, or any other framework that embeds Chromium.
  
  
# Chromium Embedded Framework
  https://en.wikipedia.org/wiki/Chromium_Embedded_Framework
  The Chromium Embedded Framework (CEF) is an open-source software framework for embedding a Chromium web browser within another application. This enables developers to add web browsing functionality to their application, as well as the ability to use HTML, CSS, and JavaScript to create the application's user interface (or just portions of it).

CEF runs on Linux, macOS, and Windows. It has many language bindings including C, C++, Go, Java, and Python.
  
  CEF 3 is a multi-process implementation based on the Chromium Content API and has performance similar to Google Chrome.[5] It uses asynchronous messaging to communicate between the main application process and one or more render processes (Blink + V8 JavaScript engine).
   The single-process run mode is not supported, but still present; currently is being used for debugging purposes only.[6]
  
  CEF comes with a sample application called CefClient that is written in C++ using WinAPI, Cocoa, or GTK (depending on the platform) and contains demos of various features.[7][8] Newer versions include a sample application called CefSimple that, along with an accompanying tutorial, show how to create a simple application using CEF 3.[9]
  
  
  
  
# How browsers work				
	Behind the scenes of modern web browsers				VIMP   TO Explore
  http://taligarsiel.com/Projects/howbrowserswork1.htm
  
  
  
  
  
  
  
  
  
  
  
  
  
  
