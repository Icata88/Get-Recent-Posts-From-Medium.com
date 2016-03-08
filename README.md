# Get-Recent-Posts-From-Medium.com
A simple way to pull a list of your recent blog posts from Medium.com

Medium is a great place to write, but when it comes to getting a list of your recent posts that you can post on your own website there aren't many good options.  

This example uses your user's RSS feed (which Medium doesn't promote) to create a list of links to your stories. You can find your feed by going to https://medium.com/feed/@yourusername.

There are a few things that I don't like about Medium's feeds, however.

- The titles of posts include the name of the publication it is included in
- The feed includes comments you make on other people's posts in addition to your stories
- The image is cropped to 600x200 and rarely looks good

Since Medium gives you no control over these things, this example uses javascript to strip that stuff out. This is brittle because if Medium changes your RSS feed (which they could do without warning at any time) it could break this hack. 

# How do I set it up?
Answer: Put the URL for your RSS feed on line 10. This should just be a matter of changing "@ade3" with your username.  

# How does it strip out comments?
Answer: It looks for images. Because your posts most likely include images and your comments most likely don't, it uses the presence of images to guess if an item is a full post or a comment. I told you it was hacky.

# Can I see the thumbnail image for a post?
Answer: Yes. Look at "index2.html" for how you could get fancy with images.

# How does the RSS feed get parsed"
Answer: that magic happens using Google's Feed API. You can read all about it at [https://developers.google.com/feed/v1/devguide](https://developers.google.com/feed/v1/devguide)

# How can I get help?
Answer: Sorry, you are on your own. 