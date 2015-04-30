![](headers/4-5.jpg)
# Introduction

In this step we will continue speaking about namespacing, which is going to allow us to access a group of code by using the namespace `commonRules`. We will style the "Team" section now.

# Styling Team section

Everything is pretty straightforward here:

```less
#team {
	#commonRules;
}
```

We are employing `commonRules` again.

Also replace placeholders with some real images in your layout:

```html
<div class='grid'>
  <div>
    <img src="images/team/ashley.png" width='250' height='250' alt='Ashley'>
    <h3>Ashley McKnilley</h3>
    <h4>Art Director</h4>
  </div>

  <div>
    <img src="images/team/jenny.png" width='250' height='250' alt='Jenny'>
    <h3>Jenny Thompson</h3>
    <h4>Web Designer &amp; Developer</h4>
  </div>

  <div>
    <img src="images/team/sarah.png" width='250' height='250' alt='Sarah'>
    <h3>Sarah Crawford</h3>
    <h4>SEO Specialist</h4>
  </div>

  <div>
    <img src="images/team/walter.png" width='250' height='250' alt='Walter'>
    <h3>Walter Miller</h3>
    <h4>General Manager</h4>
  </div>
</div>
```

Observe the result in the browser!