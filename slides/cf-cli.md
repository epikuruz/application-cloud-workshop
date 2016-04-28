# cf Command Line Interface

Command line client for Cloud Foundry - download from your space in Web Console

---

## Does it work?

```bash
$ cf
NAME:
   cf - A command line tool to interact with Cloud Foundry

USAGE:
   [environment variables] cf [global options] command [arguments...] [command options]

VERSION:
   6.12.3-c0c9a03-2015-08-31T20:29:00+00:00

BUILD TIME:
   2016-04-28 11:36:32.065750459 +0200 CEST
```



---

## Login


```bash
$ cf api api.lyra-836.appcloud.swisscom.com
Setting api endpoint to https://api.lyra-836.appcloud.swisscom.com...
OK
```

```bash
$ cf login
API endpoint: https://api.lyra-836.appcloud.swisscom.com

Email> [my-email]

Password> [my-password]
Authenticating...
OK
```


---

## Switch Space/Org

```bash
$ cf target -o ORG -s SPACE
```

---

```bash
# LIST SPACES IN CURRENT ORG
$ cf spaces

dev
prod
```


```bash
# LIST ORGS
$ cf orgs

team1
team2
```
