4. **Add the switch functionality with jquery**
The script.js file adds the switch functionality to thetoggle. So, when the user clicks the toggle, the dark mode gets applied and the label on the switch changes to ON. And, if the user clicks the toggle when the page is in dark mode, the light mode gets applied and the label changes to OFF.

```Javascript
$( ".inner-switch" ).on("click", function() {
	if( $( "body" ).hasClass( "dark" )) {
		$( "body" ).removeClass( "dark" );
		$( ".inner-switch" ).text ( "OFF" )
	} else {
		$( "body" ).addClass( "dark" );
		$( ".inner-switch" ).text( "ON" );
	}
});
```