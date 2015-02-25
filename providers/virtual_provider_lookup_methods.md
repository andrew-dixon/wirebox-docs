# Virtual Provider Lookup Methods

This is a ColdFusion 9/10 feature only, where you can mark methods in your components with a special provider annotation so they can serve the objects you requested automatically for you. This is an amazing feature as it will take the original method signature and replace the method for you with one that will serve the provided objects for you automatically. How insane is that! You deserve some <b>getting jiggy wit it (chapter 4) </b> dancing!

```javascript
public Espresso function getEspresso() provider="espresso"{}
```

Wow! That's it! Yep, just create an empty method signature and annotated with provider={mapping} and then WireBox will read these annotated methods and replace them for you at runtime so when you call getEspresso() it actually calls the WireBox injector and requests a new espresso instance and it returns it.

<br>
<div style="border: 1px solid black">
<img src="../images/icon_important.png" width="13%" style="float:left;margin-top:10px"><p style="margin:12px"><b>
Important: Please note that the visibility of provided methods does not matter to WireBox. It can provide public, private, or packaged visibilities with no problem at all. </b></p>
<div style="clear:both"></div>
</div>
<br>