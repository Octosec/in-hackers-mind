# Request methods

* GET: Passes all query material in the URL query string.
* POST: Passes all requested data in the HTTP request body.

# Response codes

* 1xx  Informational
* 100  Continue
* 2xx  Success
* 200  OK
* 3xx  Redirection
* 301  Moved Permanently
* 302  Found
* 4xx  Client Error
* 401  Unauthorized
* 403  Forbidden
* 404  Not Found
* 408  Request Timeout
* 5xx  Server Error
* 500  Internal Server Error

# Cookies

* Secure: only send over encrypted channel
* HttpOnly: prevents JavaScript from accessing the cookie

# Request with netcat, telnet

```bash
nc <target> 80
HEAD / HTTP/1.1

```

```bash
for i in `cat list.txt` ; do curl -isk -X HEAD http://$i/ > $i 2>&1 ; echo Scanned $i ; done
```
