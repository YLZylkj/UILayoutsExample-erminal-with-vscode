The Katacoda terminal layout provides a full Terminal experience. This can be extended to include a full IDE experience as a separate tab by including showide within the environment section of the index.json. For example:

"environment": {
  "showide": true
}
IDE Functionality
With the IDE, you can open files certain files from Markdown - newFile.js{{open}}

You can copy, extend or replace text from UI helpers.

var http = require('http');
var requestListener = function (req, res) {
  res.writeHead(200);
  res.end('Hello, World!');
}

var server = http.createServer(requestListener);
server.listen(3000, function() { console.log("Listening on port 3000")});
The following snippet will prepend the contents of the editor:

console.log("Starting...")
Within the Markdown, include:

<pre class="file" data-filename="app.js" data-target="prepend">console.log("Starting...")
</pre>
The following snippet will append the contents of the editor:

console.log("Finishing...")
Within the Markdown, include:

<pre class="file" data-filename="app.js" data-target="append">console.log("Finishing...")
</pre>
The editor can copy to particular files based on the data-filename attribute:

console.log("Index.js here...")
Within the Markdown, include:

<pre class="file" data-filename="index.js" data-target="replace">console.log("Index.js here...")