# Read11
## Images

- You can control the size of an image using the width and height properties in CSS, just like you can for any other box.
- Specifying image sizes helps pages to load more smoothly because the HTML and CSS code will often load before the images, and telling the browser how much space to leave for an image allows it to render the rest of the page without waiting for the image to download.
- the < img> element's align attribute, web page authors are increasingly using the float property to align images. There are two ways that this is commonly achieved:
1. The float property is added to the class that was created to represent the size of the image 
2. New classes are created with names such as align-left or align-right to align the images to the left or right of the page.These class names are used in addition to classes that indicate the size of the image.
- By default, images are inline elements. This means that they flow within the surrounding text. In order to center an image, it should be turned into a blocklevel element using the display property with a value of block. Once it has been made into a block-level element, there are two common ways in which you can horizontally center an image:
1: On the containing element, you can use the text-align property with a value of center.
2: On the image itself, you can use the use the margin property and set the values of the left and right margins to auto.
- The background-image property allows you to place
an image behind any HTML element. This could be the entire page or just part of the page. By default, a background image will repeat to fill the entire box.
- The background-repeat property can have four values:
1. repeat: The background image is repeated both horizontally and vertically (the default way it is shown if the backgroundrepeat property isn't used).
2. repeat-x:The image is repeated horizontally only.
3. repeat-y:The image is repeated vertically
only.
4. no-repeat: The image is only shown once.
- The background-attachment property specifies whether a background image should stay in one position or move as the user scrolls up and down the page. It can have one of two values:
1. fixed
The background image stays in the same position on the page.
2. scroll
The background image moves up and down as the user scrolls up and down the page.
- When an image is not being repeated, you can use the
background-position property to specify where in the
browser window the background image should be placed.
This property usually has a pair of values. The first represents the horizontal position and the second represents the vertical.
- The background property acts like a shorthand for all of the other background properties you have just seen, and also the background-color property. The properties must be specified in the following order, but you can miss any value if you do not want to specify it.
1. background-color
2. background-image
3. background-repeat
4. background-attachment
5. background-position
- Using CSS, it is possible to create a link or button that changes to a second style when a user moves their mouse over it (known as a rollover) and a third style when they click on it.
- CSS3 is going to introduce the ability to specify a gradient for the background of a box. The gradient is created using the background-image property and, at the time of writing,different browsers required a different syntax.
- To overlay text on a background image,the image must be low contrast in order for the text to be legible.
- To reduce the number of images your browser has to load, you can create image sprites.
<hr>
 
 # Practical Information
 - Search engine optimization (or SEO) is the practice of trying to help your site appear nearer the top of search engine results when people look for the topics that your website covers.
 - On-page techniques are the methods you can use on your web pages to improve their rating in search engines. The main component of this is looking at keywords that people are likely to enter into a search engine if they wanted to find your site, and then including these in the text and HTML code for your site in order to help the search engines know that your site covers these topics.
 - Off-Page Techniques: Getting other sites to link to you is just as important as on-page techniques. Search engines help determine how to rank your site by looking at the number of other sites that link to yours. They are particularly interested in sites whose content is related to yours.
 - In every page of your website there are seven key places where keywords (the words people might search on to find your site) can appear in order to improve its findability.
 - six steps that will help you identify the right keywords and phrases for your site.
 1. Brainstorm
 2. Organize
 3. Research
 4. Compare
 5. Refine
 6. Map
 - As soon as people start coming to your site, you can start analyzing how they found it, what they were looking at and at what point they are leaving. One of the best tools for doing this is a free service offered by Google called Google Analytics.
 1. Signing Up: The Google Analytics service relies on you signing up for an account at: www.google.com/analytics The site will give you a piece of tracking code which you need to put on every page of your site.
 2. How it Works Every time someone loads a page of your site, the tracking code sends data to the Google servers where it is stored. Google then provides a webbased interface that allows you to see how visitors use your site.
 3. The Tracking Code A tracking code is provided by Google Analytics for each website you are tracking. It should appear just before the closing < /head> tag. The code does not alter the appearance of your web pages.
 - The overview page gives you a snapshot of the key information you are likely to want to know. In particular, it tells you how many people are coming to your site.
 - The content link on the left-hand side allows you to learn more about what the visitors are looking at when they come to your site.
 - The traffic sources link on the left hand side allows you to learn where your visitors are coming from.
 - In order to put your site on the web you will need a domain name and web hosting. domain name,web hosting.
 - To transfer your code and images from your computer to your hosting company, you use something known as File Transfer Protocol.
 - There are a wide variety of sites that offer services commonly created by web developers (to save you having to build them yourself).
 - Many companies provide platforms for blogging, email newsletters, e-commerce and other popular website tools (to save you writing them from scratch).
 <hr>

 # Flash
 - Since the late 1990s, Flash has been a very popular tool for creating animations, and later for playing audio and video in websites.
 - Flash is no longer supported by many browsers but is an important part of history. 
 - Whether you are creating an animation or a media player in Flash, the files you put on your website are referred to as Flash movies.If you want to create your own Flash movie, you need to purchase the Flash authoring environment from Adobe.
 - Since 2005, a number of factors have meant that fewer websites are written in Flash or even use elements of Flash in their pages.
  <hr>

  # Video and Audio APIs

  - HTML5 comes with elements for embedding rich media in documents — < video> and < audio> — which in turn come with their own APIs for controlling playback, seeking, etc. This article shows you how to do common tasks such as creating custom playback controls.
  - You can review what all the HTML features do in the article linked above; for our purposes here,the most interesting attribute is controls, which enables the default set of playback controls. If you don't specify this, you get no playback controls.
  - The whole player is wrapped in a < div> element so it can all be styled as one unit if needed.
- The < video> element contains two < source> elements so that different formats can be loaded depending on the browser viewing the site.
- The controls HTML is probably the most interesting:
We have four < button>s — play/pause, stop, rewind, and fast forward.
- Each < button> has a class name, a data-icon attribute for defining what icon should be shown on each button (we'll show how this works in the below section), and an aria-label attribute to provide an understandable description of each button, since we're not providing a human-readable label inside the tags. The contents of aria-label attributes are read out by screenreaders when their users focus on the elements that contain them.
- There is also a timer < div>, which will report the elapsed time when the video is playing. Just for fun we are providing two reporting mechanisms — a < span> containing the elapsed time in minutes and seconds, and an extra < div> that we will use to create a horizontal indicator bar that gets longer as the time elapses.
-  < audio> elements have the same HTMLMediaElement functionality available to them, you could easily get this player to work for an < audio> element too. 

- Can you work out a way to turn the timer inner < div> element into a true seek bar/scrobbler — i.e., when you click somewhere on the bar, it jumps to that relative position in the video playback? As a hint you can find out the X and Y values of the element's left/right and top/bottom sides via the getBoundingClientRect() method, and you can find the coordinates of a mouse click via the event object of the click event, called on the Document object.
- 