![](headings/5.3.png)

# Slice up the sidebar if need be

Slicing up the sidebar is just like the header and footer. Our theme's homepage does not have a sidebar but the blog template does so we will use that one. There are no WordPress functions that we would need inside the sidebar file.

Enter the following code in `sidebar.php`:

```
<div class="col-lg-4">
    <aside class="right-sidebar">
        <div class="widget">
            <form class="form-search">
                <input class="form-control" type="text" placeholder="Search..">
            </form>
        </div>
        <div class="widget">
            <h5 class="widgetheading">Categories</h5>
            <ul class="cat">
                <li><i class="icon-angle-right"></i><a href="#">Web design</a><span> (20)</span></li>
                <li><i class="icon-angle-right"></i><a href="#">Online business</a><span> (11)</span></li>
                <li><i class="icon-angle-right"></i><a href="#">Marketing strategy</a><span> (9)</span></li>
                <li><i class="icon-angle-right"></i><a href="#">Technology</a><span> (12)</span></li>
                <li><i class="icon-angle-right"></i><a href="#">About finance</a><span> (18)</span></li>
            </ul>
        </div>
        <div class="widget">
            <h5 class="widgetheading">Latest posts</h5>
            <ul class="recent">
                <li>
                <img src="img/dummies/blog/65x65/thumb1.jpg" class="pull-left" alt="" />
                <h6><a href="#">Lorem ipsum dolor sit</a></h6>
                <p>
                     Mazim alienum appellantur eu cu ullum officiis pro pri
                </p>
                </li>
                <li>
                <a href="#"><img src="img/dummies/blog/65x65/thumb2.jpg" class="pull-left" alt="" /></a>
                <h6><a href="#">Maiorum ponderum eum</a></h6>
                <p>
                     Mazim alienum appellantur eu cu ullum officiis pro pri
                </p>
                </li>
                <li>
                <a href="#"><img src="img/dummies/blog/65x65/thumb3.jpg" class="pull-left" alt="" /></a>
                <h6><a href="#">Et mei iusto dolorum</a></h6>
                <p>
                     Mazim alienum appellantur eu cu ullum officiis pro pri
                </p>
                </li>
            </ul>
        </div>
        <div class="widget">
            <h5 class="widgetheading">Popular tags</h5>
            <ul class="tags">
                <li><a href="#">Web design</a></li>
                <li><a href="#">Trends</a></li>
                <li><a href="#">Technology</a></li>
                <li><a href="#">Internet</a></li>
                <li><a href="#">Tutorial</a></li>
                <li><a href="#">Development</a></li>
            </ul>
        </div>
    </aside>
</div>
```

There is not much else we need to do here until a later time we can add widgets to the sidebar area.
