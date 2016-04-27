# cf Command Line Console

Command line client for Cloud Foundry - download from your space in Web Console


---

## Login


```bash
$ cf api api.lyra-836.appcloud.swisscom.com
Setting api endpoint to https://api.lyra-836.appcloud.swisscom.com...
OK
```

```bash
$cf login
API endpoint: https://api.lyra-836.appcloud.swisscom.com

Email> [my-email]

Password> [my-password]
Authenticating...
OK
```



---

## Switch Space/Org

```bash
$cf target -o ORG -s SPACE
```
