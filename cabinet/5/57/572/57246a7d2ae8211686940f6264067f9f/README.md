# Bookmarklet

A bookmarklet is a small piece of JavaScript code that can be saved as a bookmark in a web browser. When clicked, the bookmarklet runs the code, which can perform various actions on the current webpage.

Here's how to create a simple bookmarklet:

1.  Create a new bookmark in your web browser and give it a name.
2.  In the "Location" or "URL" field, enter the JavaScript code that you want to run.
3.  Save the bookmark.

Here's an example of a bookmarklet that changes the background color of the current webpage to red:

1.  Create a new bookmark and name it "Change Color".
2.  In the "Location" field, enter the following JavaScript code:

Copy code

`javascript:document.body.style.backgroundColor='red'; void 0`

3.  Save the bookmark.

Now, whenever you click the "Change Color" bookmark, the background color of the current webpage will change to red. The `void 0` is required as in this case the code has a non-undefined return value and without the additional part the page will unload and return the result, in this case the string ‘red’.