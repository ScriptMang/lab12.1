# Reflection Questions

1. What is the difference between res.send() and res.sendFile()? When would you use one over the other?

Using res.send() sends the value within res.send as a HTTP response to the page body at 
the specified url path. When you use res.sendFile() it uses the data stored in the file like text, json, and csv and sends it to the page. Its much better for dealing with a large amount data that needs its own file.

Why is the path module necessary when serving files? What could go wrong if you just used a relative path like 'public/index.html'?

If you don't provide the path module the full path or absolute path is needed to serve the webpage you want to render.


How would you add a third page (e.g., a menu page) to this server? What steps would you take?

This is assuming the express middlware func is using the path to the public folder.
I woulld first create an tableIndex.html page inside the public's folder. 
Then I would create the route at '/tableIndex' where I use the path module to join the relative path to public/tableIndex.html to render the page.
