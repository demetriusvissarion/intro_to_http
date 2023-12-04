## Exercise One

Use Postman to send a `GET` request to the URL `https://postman-echo.com/get`
using a _query parameter_.

Update your URL field in Postman to the new URL we want to send a GET request
to.

In the "Query" tab below the URL field, set a query parameter with key `title`
and value `Welcome`. Then send the request.

You should get the following JSON response (although we've omitted the headers
for brevity in our documentation), and the status code should be `200 OK`:

```jsonc
{
    "args": {
        "title": "Welcome"
    },
    "headers": {
        // (omitted).
    },
    "url": "https://postman-echo.com/get?title=Welcome"
}
```

_You'll note that Postman automatically added the parameters at the end of the
URL, using a syntax such as `?title=Welcome` — this is the way query parameters
are sent in `GET` requests, inside the URL itself._



## Exercise Two

Close the tab to clear the data from your previous request.

Use Postman to send a `POST` request to the URL `https://postman-echo.com/post`
using a _body parameter_.

In the "Body" tab below the URL field, select the option "form-data", and set a
parameter with key `title` and value `Welcome`. Then send the request.

You should get the following JSON response, and the status code should be `200
OK`:

```jsonc
{
    "args": {},
    "data": {},
    "files": {},
    "form": {
        "title": "Welcome"
    },
    "headers": {
        // (omitted).
    },
    "json": null,
    "url": "https://postman-echo.com/post"
}
```

<details>
  <summary>:confused: My `url` is different — it says `/post?title=Welcome`</summary>

  ---

  If you're seeing this, you've probably put it in the 'Params' tab. To fix this:

  1. Close the tab to clear the request you made.
  2. Set up the request to send a POST request to `https://postman-echo.com/post`
  3. Click through to the "Body" tab — not the "Params" tab.
  4. Select `form-data`.
  5. Add a parameter with the key `title` and value `Welcome`.

  ---

</details>


Output:
{
    "args": {},
    "data": {},
    "files": {},
    "form": {
        "title": "Welcome"
    },
    "headers": {
        "x-forwarded-proto": "https",
        "x-forwarded-port": "443",
        "host": "postman-echo.com",
        "x-amzn-trace-id": "Root=1-656dbb8c-3182ec6065c24de046e30063",
        "content-length": "167",
        "user-agent": "PostmanRuntime/7.35.0",
        "accept": "*/*",
        "postman-token": "4bf284a4-4b6b-4843-8106-bee1b05267cf",
        "accept-encoding": "gzip, deflate, br",
        "content-type": "multipart/form-data; boundary=--------------------------317223347939884773109136",
        "cookie": "sails.sid=s%3AputTyawoEB4wkOFaS3BPxadTKIImwlga.I2b1qxHheRbQQvXcO9lqqavp51BZRqRjUUkq0ng%2B1TQ"
    },
    "json": null,
    "url": "https://postman-echo.com/post"
}