# XML-External-Entity-Injection-XXE-

That means the server accepts XML input, and it may allow special "entities" inside the XML to do things like:

Read files on the server (/etc/passwd)

Make requests to internal services

Leak data in the response

