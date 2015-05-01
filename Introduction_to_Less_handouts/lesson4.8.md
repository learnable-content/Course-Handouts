![](headers/4-8.jpg)
# Introduction

In this step I'm going to show you two external resources: Font Awesome and Google Fonts.

# Introduction to Font Awesome

We're going to start with Font Awesome that has been designed by the same team that created Twitter Bootstrap. Font Awesome includes a collection of 519 scalable and vector-based icons meaning that they can be customized with size, color, and weight just like any other font:

```html
<i class="fa fa-facebook-official"></i>
```

In order to have larger icons, you could use `fa-lg` that will increase the size by 33%. You can also increase size 2 times by using `fa-2x` class (other similar classes are available).

Browse the Getting Started to find the different options in order to get the necessary resources. We will use a **CDN (content delivery network)**, meaning that the required resources are hosted by an external hosting services provider (MaxCDN in this case). Use the `@import` directive:

```less
@import "https://maxcdn.bootstrapcdn.com/font-awesome/4.2.0/css/font-awesome.min.css";
```

Now the font is loaded and you can observe the result in the browser.

# Introduction to Google Font

Now let's discuss **Google Fonts**. Navigate to [google.com/fonts](http://www.google.com/fonts) to browse all the available fonts. Search for "quicksand" and once you find it click on the "quick use" icon (in the middle).

Next choose the style: light, normal, and bold. Bear in mind that this is going to increase the page load time (that you can check out on the right).

Next choose the "import" option below and copy the line of code presented by the wizard. Now just paste it into your *.less* file:

```less
@import url(http://fonts.googleapis.com/css?family=Quicksand:400,700);
```

The wizard also instructs you how to apply font family to your design. We will apply it to the whole page:

```less
html, body {
	.reset;
	font-family: 'Quicksand', sans-serif;
}
```

Go ahead and observe the changes!