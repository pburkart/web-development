# HTML Example Guide

This document contains some brief information for each of the example HTML documents in this repository. All of these examples more or less have the exact same structure. We specify the version of HTML we're using with the `<!DOCTYPE html>` tag, then we set a title, and add just a little bit of styling. You don't have to worry too much about the style portion of this yet, but all it does is center all text within the `body` so that everything remains centered. 

## Headings 

In this document you will find 6 sets of tags within the body. The first set being `<h1></h1>` and the last being `<h6></h6>`. The `<h1></h1>` header is the largest, and the `<h6></h6>` header is the smallest. Typically these are used in descending order with the main title of the page being an `<h1>` and then the various subsections being `<h2>`, `<h3>`, ..., `<h6>` depending on how many nested subsections there are. 

## Links

In this document you will only find two links. You will find one external link pointing towards Google, and one internal link pointing towards the headings.html file. When you specify a filename without a domain before it, the browser automatically assumes you're referencing an internal file residing within the same directory. If we were to specify the link as ../headings.html, it would try and find the headings.html file in the /Examples directory rather than the /HTML directory. 

## Lists

In this document you will find three different types of lists. The first list is an ordered list which prefaces each list item with a number. You can also stylize this with CSS to make them Roman numerals as well. The second list is an unordered list which simply prefaces each item with a bullet point. Styling an unordered list allows you to change the shape from a solid dot to a hollow one, or a square or triangle. 

In the definition list I forced the style to align the text to the left, as when this list is centered like it was, it's hard to distinguish between a definition and a list item. This list allows people to specify a definition for each of their list items. An example of where this could be used is in a pizza restaraunt, where you list a pizza's name and then all of it's ingredients. 

## Paragraphs

In this document you will simply find two paragraphs. Paragraphs are just bodies of text which automatically form a new line when the paragraph is closed. 

## Tables

In this document you will find 6 tables showing the course listing for each semester of the Computer Programming & Analysis program at St. Lawrence. I also force the width of these tables to equal the full width of the page as it looks better that way. 

## Final Thoughts

Feel free to experiment with these documents. Remove certain properties to see how it changes. 