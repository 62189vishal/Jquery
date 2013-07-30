Jquery
======

Jquery Demos












<$Html file$>
<!DOCTYPE html PUBLIC "-//W3C/
/DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
  <head>
		<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1">
		<title>jQuery demos</title>

		<!-- jQuery specific include files -->
		<link 	type="text/css" 		href="scripts/jquery-ui-1.8.20.custom/css/smoothness/jquery-ui-1.8.20.custom.css" rel="stylesheet" />
		<script type="text/javascript" 	src="scripts/jquery-ui-1.8.20.custom/js/jquery-1.7.2.min.js">			</script>
		<script type="text/javascript" 	src="scripts/jquery-ui-1.8.20.custom/js/jquery-ui-1.8.20.custom.min.js"></script>
		<!-- End of jQuery specific includes -->
		
		<!-- Demo specific include files -->
		<link 	type="text/css" 		href="styles/demos.css" 					rel="stylesheet" />
		<link 	type="text/css" 		href="styles/overridingjqueryuistyles.css" 	rel="stylesheet" />
		<script type="text/javascript" 	src="scripts/example1.js">	</script>
		<script type="text/javascript" 	src="scripts/example2.js">	</script>
		<script type="text/javascript" 	src="scripts/example3.js">	</script>
		<script type="text/javascript" 	src="scripts/example4.js">	</script>
		<script type="text/javascript" 	src="scripts/example5.js">	</script>
		<script type="text/javascript" 	src="scripts/example6.js">	</script>
		<!-- End of demo specific includes -->
		
		<!-- jQuery plugin includes -->
		<!-- Tooltip classes -->
		<link rel="stylesheet" href="scripts/poshytip-1.1/src/tip-yellow/tip-yellow.css" type="text/css" />
		<link rel="stylesheet" href="scripts/poshytip-1.1/src/tip-violet/tip-violet.css" type="text/css" />
		<link rel="stylesheet" href="scripts/poshytip-1.1/src/tip-darkgray/tip-darkgray.css" type="text/css" />
		<link rel="stylesheet" href="scripts/poshytip-1.1/src/tip-skyblue/tip-skyblue.css" type="text/css" />
		<link rel="stylesheet" href="scripts/poshytip-1.1/src/tip-yellowsimple/tip-yellowsimple.css" type="text/css" />
		<link rel="stylesheet" href="scripts/poshytip-1.1/src/tip-twitter/tip-twitter.css" type="text/css" />
		<link rel="stylesheet" href="scripts/poshytip-1.1/src/tip-green/tip-green.css" type="text/css" />
		<script type="text/javascript" src="scripts/poshytip-1.1/src/jquery.poshytip.js"></script>
		<!-- End of jQuery plugin includes -->

		<script type="text/javascript">
		function animateExamples()
		{
			// Showing and hiding examples
			// This illustrates hide() and toggle() [slideToggle() is similar to toggle but transitions are gradual]. show() is left to the reader to explore.
			$('div.example').find('div.content').hide();
			$('span.exampleSelector').prev().add( 'span.exampleSelector' ).click
				(
					function()
					{
						$(this).parent().next().slideToggle();
						if( $(this).parent().find( "img" ).attr( "src" ) == "images/closed.gif" )
							$(this).parent().find( "img" ).attr( "src", "images/open.gif" );
						else
							$(this).parent().find( "img" ).attr( "src", "images/closed.gif" );
					}
				);
		}

		function readyEventListener()
		{
			animateExamples();
			
			example1();
			example2();
			example3();
			example4();
			example5();
			example6();
		}
		
		$.holdReady( false );
		jQuery(document).ready( readyEventListener );	// $() is an alias for jQuery()				
		//$( readyEventListener );						// The above statement has this shortform
		</script>

	</head>

	<body>
		<div class="demoTitle" style="background-color:#98BF21">jQuery Demos</div>
		<div id="Example1" class="example">
			<div class='title'><img src="images/closed.gif" /><span class='exampleSelector'>Example 1</span> : Replacing '-' with Nil in all textboxes</div>
			<div class='content'>
				<input type="text" id="txt1" value="-" />
				<input type="text" id="txt2" />
				<input type="text" id="txt3" value="-" />
				<input type="text" id="txt4" />
				<input type="button" id="btn1" value="Replace using jQuery" />
				<input type="button" id="btn2" value="Replace using JavaScript" onClick="replaceWithNil()" />
			</div>
		</div>
		
		<div id="Example2" class="example">
			<div class='title'><img src="images/closed.gif" /><span class='exampleSelector'>Example 2</span> : Event handling on click of link</div>
			<div class='content'>
				<center>Visit the <a id="jquery" href="http://jquery.com">jQuery website</a></center>
			</div>
		</div>
		
		<div id="Example3" class="example">
			<div class='title'><img src="images/closed.gif" /><span class='exampleSelector'>Example 3</span> : Selectors in jQuery</div>
			<div class='content'>
				<table border="1px">
					<tr>
						<td>
							<div id="div1">
							I'm Div1<br/>
							Text in me : ABCD
							</div>
						</td>
						<td>
							<p id="p1">
							I'm Paragraph P1<br/>
							Text in me : PQRS
							</p>
						</td>
						<td>
							<p id="p2">
							I'm Paragraph P2
							</p>
						</td>
						<td>
							<div id="div2">
							I'm Div2
								<div id="div6">
								I'm Div6
								</div>
							<span>Span 1</span>
							<span>Span 2</span><br/>
							End of Div2
							</div>
						</td>
						<td>
							<div id="div3">
							I'm Div3
								<div id="div4">
								Div4
									<div id="div5">
									Div5
									</div>
								End of Div4
								</div>
							</div>
						</td>
					</tr>
					<tr>
						<td>Name :<br/><input type="text" name="txtName"/></td>
						<td>
							Gender :<br/>
							<input type="checkbox" name="chkM"/> M<br/>
							<input type="checkbox" name="chkF" name="chkF"/> F
						</td>
						<td>E-mail :<br/><input type="text" name="txtEmail"/></td>
						<td>Company's name :<br/><input type="text" name="txtCompanyName"/></td>
						<td>
							Membership type :<br/>
							<input type="radio" name="rdMemType" id="monthly"/> Monthly<br/>
							<input type="radio" name="rdMemType" id="annual"/> Annual
						</td>
					</tr>
					<tr>
						<td colspan="5" align="center">
							<select id="chSelector">
								<option value="">--Choose selector--</option>
								<option value="Selection based on text contained within a node<br>Select all divs that contain the text 'ABC'">
									$("div:contains('ABC')")
								</option>
								<option value="Filtering out nodes based on some criteria<br>Select all paras that but not the one having id='p1'">
									$("p").not("#p1")
								</option>
								<option value="Selection based on existence of a particular descendant<br>Select ancestor divs that have a div as descendant">
									$("div:has(div)")
								</option>
								<option value="Selection based on non-existence of a particular descendant<br>Select ancestor divs that do not have a div as descendant">
									$("div").not(":has(div)")
								</option>
								<option value="Select an element following a particular element<br>Select every span that follows a div">
									$("div+span")
								</option>
								<option value="Selection of descendants based on existence of a particular ancestor<br>Select all spans within divs">
									$("div span")
								</option>
								<option value="Attribute value [input type='checkbox']">
									$("input[type='checkbox']")
								</option>
								<option value="Part of attribute [name has 'Mem']">
									$("input[name*='Mem']")
								</option>
								<option value="Start of attribute [id starts with 'btn']">
									$("input[id^=btn]")
								</option>
								<option value="Ending of attribute [nam ends with 'Name']">
									$("input[name$='Name']")
								</option>
								<option value="Parent [Div > Span]">
									$("div&gt;span")
								</option>
								<option value="Predecessor [Div ~ Span]">
									$("div~span")
								</option>
								
							</select><br/>
							<span id="selectorDesc"></span>
							<br/>
							Enter your own selector : 
							<input type="text"	 id="txtSelect" />
							<input type="button" id="btnSelect" value="Select" />
						</td>
					</tr>
				</table>
			</div>
		</div>
		
		<div id="Example4" class="example">
			<div class='title'><img src="images/closed.gif" /><span class='exampleSelector'>Example 4</span> : Important methods in jQuery</div>
			<div class='content'>
				<div class="outerElement">
					<div class="innerElement" id="divInnerElement">div</div>
					<p 	 class="innerElement" id="pInnerElement">p</p>
					<span>A span. <b>Methods show(), hide() and toggle() are illustrated by the very way this demo has been coded to show and hide examples.</b></span>
				</div><br/>
			
				<span class="button" id="btnSetHTML" 			title="Set innerHTML for div and p">html()</span>&nbsp;
				<span class="button" id="btnSetHTMLPreserve" 	title="Set innerHTML for span with markup preserved">text()</span>&nbsp;
				<span class="button" id="btnSetAttribute"		title="Get attribute id for div and p and Set attribute class for span to 'innerElement'">attr()</span>&nbsp;
				<span class="button" id="btnAppendDiv"	  		title="Append a div element to outer div">appendTo()</span>
			</div>
		</div>
		
		<div id="Example5" class="example">
			<div class='title'><img src="images/closed.gif" /><span class='exampleSelector'>Example 5</span> : CSS Manipulation</div>
			<div class='content'>
				<p>This is a paragraph</p>
				<div style="width : 25%" class="red">This is a div with default style='red'</div><br/>
				
				<span class="button" id="btnAddStyle" 			title="Add style to p">css()</span>&nbsp;
				<span class="button" id="btnAddStyleClass" 		title="Add style class (red) to p">addClass()</span>&nbsp;
				<span class="button" id="btnRemoveStyleClass" 	title="Remove style class (red) from p and then add class (blue)">removeClass()</span>&nbsp;
				<span class="button" id="btnToggleStyleClass" 	title="Toggle style class (between red [default] and blue) for div">toggleClass()</span>&nbsp;
				<span class="button" id="btnAnimate" 			title="Animate">animate()</span>
			</div>
		</div>
		
		<div id="Example6" class="example">
			<!-- Tabs -->
			<div class='title'><img src="images/closed.gif" /><span class='exampleSelector'>Example 6</span> : jQuery UI Components</div>
			<div class='content'>
				Click here to view <a href="./scripts/jquery-ui-1.8.20.custom/index.html" target="_blank">jQuery UI Demos</a> found in the development bundle folder.
				&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
				<input type="button" id="toggleTabState" value="Enable jQuery Mobile tab" />
				<input type="button" id="addTab" 		 value="Add new tab" />
				<br/><br/>
			
				<h3>jQuery Session Feedback and References</h3>
				<div id="tabs" class='bodystyle'>
					<ul class='bodystyle'>
						<li><a href="#tabs-feedback">Feedback</a></li>
						<li><a href="#tabs-jQueryUI">jQuery UI official website</a></li>
						<li><a href="#tabs-jQueryMobile">jQuery Mobile official website</a></li>
					</ul>
					<div id="tabs-feedback" class='bodystyle'>						
						<!-- Accordion -->
						<div id="accordion">
							<h3><a href="#"><b>Participant and Training details</b></a></h3>
							<div id="accordionKey">
								<table>
									<tr>
										<td>Participant's Business unit</td>
										<td><input type="text" id="txtBU" title="Enter one of Infosys' BUs"/></td>
									</tr>
									<tr>
										<td>Participant's DC</td>
										<td><input type="text" id="txtDC" title="Enter one of Infosys' DC locations"/></td>
									</tr>
									<tr>
										<td>Training start date</td>
										<td><input type="text" id="txtStart" /></td>
									</tr>
									<tr>
										<td>Training end date</td>
										<td><input type="text" id="txtEnd" title="Make sure you enter a date that comes after the start date"/></td>
									</tr>
								</table>
							</div>
							<h3><a href="#"><b>Course Content</b></a></h3>
							<div id="accordionKey">
								<table>
									<tr>
										<td>Relevance of topics taught</td>
										<td width="200px"><div id="contentSlider1"></div></td>
										<td>&nbsp;&nbsp;<span id='ratingValue1'></span></td>
									</tr>
									<tr>
										<td>Variety of topics</td>
										<td width="200px"><div id="contentSlider2"></div></td>
										<td>&nbsp;&nbsp;<span id='ratingValue2'></span></td>
									</tr>
									<tr>
										<td>Coverage of material in a topic</td>
										<td width="200px"><div id="contentSlider3"></div></td>
										<td>&nbsp;&nbsp;<span id='ratingValue3'></span></td>
									</tr>
									<tr>
										<td>Clarity of content</td>
										<td width="200px"><div id="contentSlider4"></div></td>
										<td>&nbsp;&nbsp;<span id='ratingValue4'></span></td>
									</tr>
								</table>
							</div>
							<h3><a href="#"><b>Course delivery</b></a></h3>
							<div id="accordionKey"></div>
							<h3><a href="#"><b>Comments</b></a></h3>
							<div id="accordionKey">Any additional comments may be given in the space below<br/><textarea></textarea></div>
						</div>
						<br/>
						
						<!-- Button -->
						<center><button id="button">Submit feedback</button></center>
					</div>
					<div id="tabs-jQueryUI">	<iframe src="http://jqueryui.com" 		height="500px" width="100%" frameborder="0"></iframe></div>
					<div id="tabs-jQueryMobile"><iframe src="http://jquerymobile.com" 	height="500px" width="100%" frameborder="0"></iframe></div>
					<div id="tabs-w3schools" class="ui-helper-hidden">		<iframe src="http://www.w3schools.com/jquery/default.asp" 		height="500px" width="100%" frameborder="0"></iframe></div>
				</div>
			</div>
		</div>
	</body>
</html>

