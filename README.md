# JS-http-to-ts3server
Converts a http URL to a ts3server URL.

# Why?
Many games and chat programs do not support application URLs but do support opening web page URLs.
This creates a simple fix to that problem by allowing a standard http URL to be shared.

# Usage
The script uses html GET request for it's parameters.
  NONE are required.
#### 's' is Server
* If 's' is not provided, the script will assume the web server domain is the same as teamspeak. For example, ```http://example.com/ts.html``` would redirect to ```ts3server://example.com```
* If 's' contains no periods but has text, it will assume a subdomain, For example, ```http://example.com/ts.html?s=sub``` would redirect to ```ts3server://sub.example.com```
* If 's' contains periods, it is assumed you are defining a full domain name.

#### 'p' is Password
* if p is provided a password will be appended to the url. For example,```http://example.com/ts.html?p=goodpass``` would redirect to ```ts3server://example.com?password=goodpass```

#### 'n' is Bookmark Name
* ```http://example.com/ts.html?n=My%20Teamspeak%20Server``` would redirect to ```ts3server://example.com?addbookmark=My%20Teamspeak%20Server```

 #### Any combination would be valid.
* if 'n' and 'p' where provided, both arguments would be passed. For example, ```http://example.com/ts.html?p=goodpass&n=My%20Teamspeak%20Server``` would redirect to ```ts3server://example.com?password=goodpass&addbookmark=My%20Teamspeak%20Server```
