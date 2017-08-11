# Examples

## Date Examples

```
https://us-central1-<project-id>.cloudfunctions.net/date

https://us-central1-<project-id>.cloudfunctions.net/date?format=MMMM%20Do%20YYYY%2C%20h%3Amm%3Ass%20a
```

You can also send the format in the request body. For instance using cURL in the command line:

```
curl -H 'Content-Type: application/json' /
     -d '{"format": "MMMM Do YYYY, h:mm:ss a"}' /
     https://us-central1-<project-id>.cloudfunctions.net/date
```

Formatted dates should be displayed.

We are responding with a 403 error in case of PUT requests:

```
curl -X PUT -d '{"format": "MMMM Do YYYY, h:mm:ss a"}' https://us-central1-<project-id>.cloudfunctions.net/date
```
