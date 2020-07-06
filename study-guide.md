# Study Guide

This is my study guide for COMP 205 - Web Development.

## Introduction
In COMP 205 - Web Development you will be learning the basics about how webpages actually function. For people who are new to web development and programming in general, this may seem daunting at first. But overtime creating basic webpages with HTML and CSS will be like second nature to you. 

Simple webpages are created using a combination of HTML (HyperText Markup Language) and CSS (Cascading Style Sheets). HTML is what gives a webpage it's content, such as text and images. CSS on the other hand is what gives a webpage its style, such as background color, positioning and sizing of elements, and fonts. 

More modern webpages extend their functionality by introducing an additional programming language known as JavaScript. JavaScript is a powerful scripting language which enables developers to easily add all kinds of functionality to their site. For example, an animated timestamp indicating the current time in a webpage would have been created using JavaScript, in order to continuously update the content of the element to reflect the current time. 

In this course we are primarily going to be focusing on just HTML and CSS, in order to familiarize ourselves with the basics. However we are going to briefly touch on JavaScript when we incorporate a timestamp into our website. 

This document has been divided into 5 sections: An introduction, HTML, CSS, JavaScript, and some closing thoughts. 

## HTML
HTML is the language that is used in order to create webpages. It provides a webpage with the content, but doesn't do anything in the way of stylizing that content. A website made entirely in HTML would look not much different than the text document you're reading now, with larger and smaller fonts. 

In order to start writing HTML, all someone needs to do is open up a text editor (such as Notepad), write their HTML, and save the file as filename.html. The filename can be whatever you like, but the .html extension is important. Make sure that it isn't being saved as filename.html.txt. Once you have your HTML file you can simply find it in your file explorer and drag it into your browser.

HTML is made up of what are known as "tags". Most tags come in pairs, with an opening tag, and a closing tag, and any relevant content in between. For example, in order to create a paragraph we use the `<p>` opening tag to start the paragraph, and then the `</p>` closing tag to finish it. Any text in between those tags would be displayed on the website as a paragraph. 

In addition to paragraphs, some of the other commonly used elements found in the body of a webpage are headers (Largest to Smallest: `<h1></h1>`, `<h2></h2>`, ..., `<h6></h6>`), images (`<img src="path-to-file"/>`), and lists (`<ol></ol>`, `<ul></ul>`, `<dl></dl>`), but there are loads more. Make sure to check out the "Next Steps" document for more. 

For the elements that I've listed above, while all of these will work on their own, there are a few other elements that you need to create in order to have a proper webpage. In an actual webpage, it is structured in a particular way so that the web browser knows whats what. The elements above would all be found in the `<body>` section of the webpage. All content that you see displayed on the screen is inside of the `<body></body>` tags.

The body of the webpage itself resides within the `<html></html>` tags of the webpage. Everything within these tags will be interpreted by your web browser as a single HTML document. The final major section of every webpage is the `<head></head>`. The elements in here primarily describe the website, and the resources it uses. You'll find the `<title></title>` tag which gives your webpage the title that appears in the tabs in your browser. You'll find `<meta>` tags which describe certain properties of the webpage such as the author and description. And you'll find a `<link>` to a CSS document which gives your webpage its style (which we'll talk about in the next section of this document).

With the above information, lets now look at a very simple example of a webpage.

```
<html>
  <head>
    <title>Simple Webpage</title>
  </head>
  <body>
    <h1>Webpage Title</h1>
    <p>This is just a simple paragraph.</p>
  </body>
</html>
```

This might look a little messy at first, but lets break it down. The entire HTML document is wrapped in the `<html></html>` tags, as you can see there's one at the top and one at the bottom. Below the opening `<html>` tag you'll see the start of the `<head></head>` block of code. Inside of this you'll see we have the title of our webpage set as "Simple Webpage". This is the text that will appear in the tab in your browser. For example, in this current tab you most likely see "web-development/study-guide.md at master · pburkart/web-development". 

Below this in the `<body></body>` block of our HTML document we have two elements. A `<h1></h1>` header, which is the largest of the predefined headers, and a `<p></p>` paragraph element. Inside the header we have the webpage title set simple to "Webpage Title", and the paragraph set to "This is just a simple paragraph.". As you can see already, HTML is a fairly straight forward tool to learn how to use, and with enough time it will be easy to master. 

The final element that I'd like to cover in this document which is relevant to the scope of this course, is the link. Links "link" one webpage to another, allowing a user to easily go from one webpage to the next, without having to manually type the URL into their address bar. Links are defined using the `<a></a>` element, and look like this: `<a href='https://google.ca/'>Click Me to Google</a>`

This link when clicked would take you to Google's homepage. Links are an important tool when building webpages for a whole variety of reasons, primarily ease of use for the end user. 

## CSS
CSS is the language that is used when building webpages in order to style them. For example, on this current webpage you'll see the dark navagation bar along the top of the webpage. In order to create this, the developer responsible applied a `background-color` "property" to the `<header></header>` element. In CSS there are multiple ways of specifying colors, but for the purpose of this document, and most likely throughout this course, we will be using what are known as Hex, or Hexidecimal, color codes. 

In this semester you'll also be taking Introduction to Computer Mathematics so it may prove beneficial to understand how these work. These codes are comprised of 6 numbers, with each pair representing the colors Red, Green, and Blue respectively. They are known as Hex color codes because they use the hexidecimal numbering system. Let's look at an example of a color code. `#24292e` is the color code that is used for the dark bar at the top of the screen. The `#` at the start indicates to the web browser that it is a hexidecimal color code. We then have the value 24292e. This can be interpreted as 24 for Red, 29 for Green, and 2e for Blue. Since we are raised with the base-10 decimal numbering system, this may seem a little odd at first, but once we understand how it works it will make sense. Hexidecimal uses a Base-16 numbering system. What this means, is that instead of counting from 0-9 like we do with our Base-10 Decimal System (10 for 10 digits), we count from 0 to F (or 16 digits). 

The way we count in Hexidecimal is a little different than decimal, but once you understand the pattern it's easy. We start by counting from 0 to 9 as we normally would, and then instead of going up to 10, we start counting at A all the way to F. So the first 16 digits of the hexidecimal numbering system look like this: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F. With the decimal numbering system when you get to 9, you add a 1 to the start and go back to 0. With hexidecimal when you get to F, you add a 1, and go back to 0. So in hexidecimal, 10 is actually 16 in Decimal, since the 16th number (not including 0) is 10. Then you would repeat the pattern; 11, 12, 13.. 1A, 1B, 1C.. 1F, 20, 21, etc.

Going back to the hexidecimal value from before of `#24292e`, we can now break this down and understand how it correlates to the color it does. As we already know, the three pairs of numbers correlate to Red, Green, and Blue. Knowing that it is using the hexidecimal numbering system, we can then figure out that the three values are 36, 41, and 46. But what do these numbers mean? Knowing that it is using the hexidecimal numbering system and that is comprised of pairs you can figure out that each value has a range of 0 to 255. These values represent the intensity of the individual colors. If you had a hexidecimal value of #000000 it would be black, and conversly if it was #ffffff it would be white. If the Red, Green, and Blue values are equal or close to each other, you will end up with a gray color. Depending on how close it is to white or black will change the shade of gray. In this case, since the values are on the lower end of the 0-255 value range, you end up with a darker gray color. 

CSS itself is far greater in complexity when compared to HTML. With such a large number of desired outcomes, the possibilities of what you can do with CSS are nearly endless. For the purpose of this document, we will only be covering a few CSS properties which will most likely be relevant to this course. The properties that we'll be covering are: `background-color`, `color`, `font-family`, `font-size`, `text-align`, `margin`, `padding`, `border`, and `border-box`. 

Firstly, let us look at how we can actually go about writing CSS and applying it to our webpage. CSS documents can be compiled inside of a text editor such as notepad, same as HTML. For CSS documents they must be saved with the .css file extension. File names don't matter, but typically I name mine style.css. Once you have the .css file created, you need to link it in your webpage. In order to do this, we'll need to use the `<link>` tag that we talked about in the previous section. In order to link a css file stored in the same directory (folder) as the html file with the name style.css, we need to include the following line in our HTML: `<link rel='stylesheet' type='text'/css' href='style.css'/>`

Note that with this tag we don't have to specify a closing `</link>` tag. That is because this tag doesn't expect to be wrapped around any content, and so it functions as it should on its own. By specifying the / at the end of the tag, it closes itself. In this `<link>` element, the `rel` property specifies the relationship the document has with the browser, the `type` property specifies the type of document that it is, and the `href` property specifies where to locate this resource. This line of code goes inside of the head section of our webpage like so:

```
<html>
  <head>
    <title>St. Lawrence College</title>
    <link rel='stylesheet' type='text/css' href='style.css'/>
  </head>
  <body>
    <h1>St. Lawrence College</h1>
    <p>Computer Programming & Analysis</p>
  </body>
</html>
```

Now that we have our webpage linked up to our CSS file, we can start writing some code. We are going to take the above HTML and style it, specifying a background color, centering the text, changing the color of the font and the font type, then we'll do a little bit of positioning on the elements and draw a border around it. If you can follow this next section, you'll be well on your way to mastering this course. 

When writing CSS we don't write tags like we do with HTML. Instead, we specify the element that we are styling using a selector, and then use property-value pairs to style different properties of the element. For example, in order to set the `font-size` for all paragraphs to 14px, we would write the following CSS.

```
p {
  font-size: 14px;
}
```

Now all paragraphs in our webpage will have a `font-size` of 14px. In this css the `p` at the start is the selector, and tells the web browser you are selecting all `<p></p>` tags. The curly braces which encompass the rest `{ }` define the block of CSS pertaining to that selector. Our property in this case is `font-size` and the value for that property is 14px. We end the line with a semi-colon, indicating that it is in fact the end of that line of CSS. Since it is the last line of CSS in the `p` block, the semi-colon isn't actually neccessary since it is closed by the closing curly brace `}`, but it's good practice to get into. 

Now that you have a basic understanding of how to write CSS, let's go ahead and style our webpage taking it line by line. 

First we're going to want to change the background color of our webpage to something a little less harsh on the eyes. For the purposes of this demonstration I picked the color #222222 which is a dark gray. In order to specify this, we'll need to open the body selector, and then specify #222222 as the value for the `background-color` property. This looks like this:

```
body {
  background-color: #222222;
}
```

If you save these changes and reload the webpage in your web browser you will see that instead of a white color, the background is now a dark gray. However because we made the background darker, the text on the screen is more difficult to read since it is also dark. To fix this we're going to change it to white, which can be done with the following line: `color: white;`. Note that we can simply use the word "white" as opposed to the hex code #ffffff. We can do this because the developers of CSS have included certain preset colors that can be referenced. Insert this line of CSS below the `background-color: #222222;` line but above the closing curly brace `}`. 

The next thing that we are going to want to change is the font type. Currently it is using a Serif font (you can tell by the small little designs at the tips of the letters rather than straight flat lines, these are called serifs). Serif fonts are primarily only good for fancy logos or headers, or for stylizing certain paragraphs of text a particular way. For the most part you'll want to use `sans-serif` fonts when designing websites, as they'll make the website more visually appealing. The `sans-serif` font that we want to use is Arial, but depending on the user's browser this may for what ever reasons not be available, so we have to specify additional fonts to fall back on in case it can't find the first one. This can be done with the following line of CSS, which again, goes below the last line of CSS you wrote: `font-family: Arial, Helvetica, sans-serif;`

This line of CSS first tries to set the `font-family` property to the value of `Arial`. If it can't find the Arial font type then it will try and use Helvetica, and if that doesn't work it will use what ever sans-serif font it has available. 

Now we have styled our font so it looks a little bit better but it's all the way over on the top left corner of our screen. Let's fix that. We can center the text to the middle of our screen by assigning the `center` value to the `text-align` property, like so: `text-align: center;`. This will move the `<h1></h1>` element to the center of its parent element, which in the case is the `body`. This will cause the text to be centered in the middle of the screen since it fills the width of the screen. However if you had the header nested inside of another element, and that element was given positional styling as well, it may not center in the middle of the screen. For the purposes of this demonstration however this will work just fine. 

Your CSS file should now in its entirety look like this:

```
body {
  background-color: #222222;
  color: white;
  font-family: Arial, Helvetica, sans-serif;
  text-align: center;
}
```

This is all the styling that we'll need to do for the body, but now we're going to do some additional styling for the `<h1></h1>` element as well. The firt thing we are going to do is specify some margins. Currently we have it in the middle of the screen, but it is stuck to the top of the webpage which doesn't look the greatest. Additionally, although the user can't see it, currently the h1 element takes up the entire width of the screen like a thing rectangle the height of the text. Later on we are going to be specifying a border, so we are going to want to reduce the width of the element so that the border doesn't stretch from one side to the other. To apply the margins, we can write the following line of CSS: `margin: 5em 15em 0 15em;`

This may look a little confusing at first but lets break it down. The margin property adds space between the edge of one element, and any other elements on the top, left, bottom, or right. The unit of measurement we are using for these margins is the width of the letter m in the current settings. This allows for more consistent measurements since the number of pixels varies depending on screen resolution. There are a few ways we can use the margin command in order to specify the different margins. Specifying it the way we did allows us to specify the 4 margins individually, but if we wanted to specify a margin of 5em for all four sides, we could have simply wrote `margin: 5em`. Or if we wanted a margin of 5em on the top and bottom, and 10em on the left and right, we could have wrote `margin: 5em 10em`. When we write out all four margins, we are specifying the values for the top, left, bottom, and right margins respectively. So in this case we are specifying a margin of 5em for the top, 15em for the left, no margin for the bottom, and a margin of 15em for the right. This will give us some space on the top, reduce the width on of the element, while leaving the paragraph unchanged.

In addition to the margins which add space on the outside of the element, we can also specify the padding, which adds space to the inside of the element. In order to increase the gap between our `<h1></h1>` and the border that will surround it, we are going to increase the padding to 5px with the following line of CSS: `padding: 5px;`. Now instead of the border sticking right to the top and bottom of our text, there will be a gap which looks a little nicer. 

Next up we'll want to specify a border. A border is a line that surrounds the element. A border is made up of 3 values. The width, the type, and the color. For our border we are going to use a width of 3px, the solid border type, with a black color. The syntax for this looks like so: `border: 3px solid black;`. After saving these changes you should see a black line appear around the outline of our element. If you remove the 15em margins on the left and right, you'll see that border stretch all the way across the screen. 

The final line of CSS that we are going to specify is the `border-radius`. The border radius is effectively the amount of vertical distance it takes for it to turn 90 degrees. By default it is set to 0 which is why you see the sharp right angles on it's corners. If we set the border to 5px, it would take 5px for it to rotate that 90 degrees, giving it a curved effect. The more we increase the `border-radius`, the longer and more pronounced the curve will be. For the purposes of this webpage we are going to be specifying a border of 25px. This will look like this: `border-radius: 25px;`.

Now that we have finished writing the CSS, the file should look like this:

```
body {
  background-color: #222222;
  color: white;
  font-family: Arial, Helvetica, sans-serif;
  text-align: center;
}

h1 {
  margin: 5em 15em 0 15em;
  padding: 5px; 
  border: 3px solid black;
  border-radius: 25px;
}
