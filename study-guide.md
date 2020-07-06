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

