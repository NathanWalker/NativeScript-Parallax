#NativeScript Parallax View Plugin for Android & iOS.


###Parallax Scroll
[![NativeScript Parallax Scroll Effect. Click to Play](https://img.youtube.com/vi/sR_Ku7dsm2c/0.jpg)](https://www.youtube.com/embed/sR_Ku7dsm2c)
###Parallax Scroll with Anchor.
[![NativeScript Parallax Scroll Effect. Click to Play](https://img.youtube.com/vi/uQsZr7PyGSM/0.jpg)](https://www.youtube.com/embed/uQsZr7PyGSM)
###Install
`$ tns plugin add nativescript-parallax`

###Example xml useage

```xml
<Page xmlns="http://schemas.nativescript.org/tns.xsd"
	 xmlns:parallax="nativescript-parallax"
	loaded="pageLoaded">
  	<parallax:ParallaxView controlsToFade="headerLabel,headerLabel2">
		<parallax:Header class="header-template">
			<Label id="headerLabel" text="Parallax"></Label>
			<Label id="headerLabel2" text="Component"></Label>
		</parallax:Header>
		<parallax:Anchored class="anchor">
			<Label id="titleLabel" text="Parallax Template"></Label>
		</parallax:Anchored>
		<parallax:Content class="body-template">
			<TextView editable="false" text="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut scelerisque, est in viverra vehicula, enim lacus fermentum mi, vel tincidunt libero diam quis nulla. In sem tellus, eleifend quis egestas at, ultricies a neque. Cras facilisis lacinia velit ut lacinia. Phasellus fermentum libero et est ultricies venenatis sit amet ac lectus. Curabitur faucibus nisi id tellus vehicula luctus. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nunc condimentum est id nibh volutpat tempor. Phasellus sodales velit vel dui feugiat, eget tincidunt tortor sollicitudin. Donec nec risus in purus interdum eleifend. Praesent placerat urna aliquet orci suscipit laoreet. In ac purus nec sapien rhoncus egestas.

			Ut at consequat libero, at pharetra purus. Integer mi lorem, luctus eget porttitor vitae, pharetra et urna. Morbi et euismod lacus. Vestibulum a massa odio. Aenean at neque hendrerit, consequat sem et, congue mi. Sed egestas, ante feugiat lacinia tempus, lacus lorem laoreet magna, a hendrerit augue leo vitae risus. Integer ornare odio nec libero elementum malesuada. Cras sem sapien, aliquet eget nibh molestie, finibus dictum augue. Nulla mi metus, finibus id arcu nec, molestie venenatis libero. Morbi a pharetra odio. Maecenas viverra, quam at sollicitudin sodales, diam purus lacinia dolor, vitae scelerisque erat mi nec nibh. Quisque egestas et nunc in pharetra. Sed vitae tincidunt justo, dictum tincidunt nisi. Quisque tempus dolor urna, et mattis velit porta vitae.">
			</TextView>
		</parallax:Content>
	</parallax:ParallaxView>
</Page>

```
###Example css
```css
#headerLabel2
{
	font-size: 45;
	horizontal-align: center;
	margin-top:-25;
	color:#B2EBF2;
}
#headerLabel{
	font-size: 45;
	horizontal-align: center;
	padding-top:75;
	color:#B2EBF2;
}
.header-template{
	background-color:#212121;
	background-image:url('~/images/mountains.png');
	background-size: cover;
	height: 200;
}
.body-template TextView{
	font-size:20;
	padding:5 15;
	border:none;
}
.anchor{
	height: 55;
	width:100%;
	background-color:#616161;
}
#titleLabel{
	font-weight:bold;
	font-size:25;
	padding:5 15;
	color:#fff;

}
```
To use the parallax plugin you need to first import it into your xml layout with  `xmlns:parallax="nativescript-parallax"`

when using the parallax plugin you need at least two layout views inside of the ``<parallax:ParallaxView>`` element. ``<parallax:Header>`` and ``<parallax:Content>``. there is an optional third view called
``<parallax:Anchored>`` which will positions it's self below the Header and once it reaches the top of the screen anchor it's self there.

To add views such as labels you want to fade out in the ``<parallax:Parallaxiew>`` add the ``controlsToFade`` attribute and pass it a comma delimited string with each control ID you want to fade out. In the above example it looks like ``controlsToFade="headerLabel,headerLabel2"`` and will fade out both of those labels.

The ``<parallax:Anchored>`` has a property called `dropShadow` if set to true it will create a small drop shadow effect on the bottom of the anchor.

If the inner content of ``<parallax:Content>`` isn't long enough to cause the page to scroll. If not it will not show the Parallax effect.

As of version 1.1.0 the bounce/overscroll effect is disable by default to turn it back on set `bounce=true` on the ParallaxView element.
###Plugin Development Work Flow.

* Clone repository to your machine.
* First run `npm install`
* Then run `npm run setup` to prepare the demo project
* Build with `npm run build`
* Run and deploy to your device or emulator with `npm run demo.android` or `npm run demo.ios`


###Special thanks to:
 [Nathanael Anderson](https://github.com/NathanaelA) for helping with understand how plugins in {N} work.
 Also Thanks to [Nathan Walker](https://github.com/NathanWalker) for setting up the {N} plugin seed that I used to help get this plugin up and running. More info can be found about it here:
https://github.com/NathanWalker/nativescript-plugin-seed

##License

[MIT](/LICENSE)