# Get-Recent-Posts-From-Medium.com
A simple way to pull a list of your recent blog posts from Medium.com

Medium is a great place to write, but when it comes to getting a list of your recent posts that you can post on your own website there aren't many good options.  

This example uses your Medium user's RSS feed (which Medium doesn't promote) to create a list of links to your stories. If you didn't know you had an RSS feed, you can find it by going to https://medium.com/feed/@yourusername.

There are a few things that I don't like about Medium's RSS feed, however.

- The titles of posts include the name of the publication it is included in
- The feed includes comments you make on other people's posts
- The post's thumbnail image is cropped to 600x200 which rarely looks good

Since Medium gives you no control over these things, this example uses javascript to strip that stuff out. This is brittle because if Medium changes your RSS feed (which they could do without warning at any time) it could break this hack. 

# Examples in action:
Basic Text version:
[http://design.adrian3.com/Medium-RSS-Feeds/index.html](http://design.adrian3.com/Medium-RSS-Feeds/index2.html)

Responsive layout with images:
[http://design.adrian3.com/Medium-RSS-Feeds/index2.html](http://design.adrian3.com/Medium-RSS-Feeds/index2.html)

# How do I set it up?
Answer: In the index file, put the URL for your RSS feed on line 10. This should just be a matter of changing "@ade3" with your username.  

# How does it strip out comments?
Answer: It looks for images. Because your posts most likely include images and your comments most likely don't, it uses the presence of images to guess if an item is a full post or a comment. I told you it was a hack.

# Can I see the thumbnail image for a post?
Answer: Yes. Look at "index2.html" for how you could get fancy with images.

# How does the RSS feed get parsed?
Answer: that magic happens using Google's Feed API. You can read all about it at [https://developers.google.com/feed/v1/devguide](https://developers.google.com/feed/v1/devguide)

# What's the slabtext.js file? Do I need it?
Answer: No. This is used in the index2.html example to make the text fit the width of the image container. You can learn more about slabtext.js at [http://freqdec.github.io/slabText/](http://freqdec.github.io/slabText/)

# How can I get help?
Answer: Sorry, you are on your own. I am not actively supporting this code, just sharing it as a starting point. Please use, remix, and improve. 