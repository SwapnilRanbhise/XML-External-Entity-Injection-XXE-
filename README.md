# XML-External-Entity-Injection-XXE-

That means the server accepts XML input, and it may allow special "entities" inside the XML to do things like:

Read files on the server (/etc/passwd)

Make requests to internal services

Leak data in the response

Analyze how data is submitted
You looked at the HTML source and saw this:

html
Copy
Edit
<form class="detailForm" action="/data" method="POST">
  <input required type="hidden" name="ID" value="1">
  <button type="submit">Details</button>
</form>
So when we click "Details", the browser sends a POST request to /data with ID=1, ID=2, or ID=3.

But what format is the request in? Since the hint mentioned XML and SOAP, we assumed the server processes XML.
