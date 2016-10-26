# Explicit Values for ARIA "state" Attributes

For boolean ARIA attributes (otherwise known as ARIA "state" attributes), 
we need to 
[explicitly have "true" or "false" assigned](https://www.w3.org/TR/wai-aria/appendices#typemapping) 
to the attribute in the DOM.

This might appear as a stark contrast to the more common case of
[using HTML attribute presence to signify a state](https://www.w3.org/TR/2008/WD-html5-20080610/semantics.html#boolean), 
but it's totally legit -- and most likely necessary for ARIA spec compliance.  

