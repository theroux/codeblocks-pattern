# codeblocks-pattern
For Shawn

The "Workshop" demo site is a great start.

However it's much more simplistic than many of our flagship sites.

Adding a modules folder is just adding a layer of complexity to help keep our code DRY.

On the main.twig file the logo, nav, and footer are now inside of blocks, and the blocks contain an includes to the module markup. 

Putting *every* piece of modular code into a block gives us more flexibility. If a certain page needs a different logo, for example, the logo on that page can be easily overwritten. Additionally, storing the module markup inside includes shortens the length/complexity of the "main.twig" file.

If this was a full-blown AMP site instead of a demo, the "main.twig" file would be very cumbersome without the use of includes.

Additionally I added a module called "Featured Content."

On the permalink page, the featured content module is not needed, so its codeblock is empty.

The "featured content" module is used on both the home page and the category pages, however.

In list-post.twig (Category page), the content is pulled from "Category Page Featured Content Zone." It's a normal AMP post.

In home.twig (Home page), the content is pulled from "Home Page Featured Content Zone." It's actually a content template post, so the data structure is a little different.

However, both are able to share the same markup (modules/featuredcontent.twig).

