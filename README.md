# updatedns

Based on https://github.com/cloudflare/python-cloudflare/blob/master/examples/example_update_dynamic_dns.py

```pip install cloudflare```

Create an API key on cloudflare, giving it the following permissions:
- Account.Account Settings (Read)
- Zone.Zone Settings (Read)
- Zone.Zone (Read) 
- Zone.DNS (Edit)

Add the API key to `.cloudflare.cfg` in the python folder

```
[CloudFlare]
token = <your api token here>
```

## Using script
Add to crontab
```*/5 * * * * updatedns.py <domain name here>```
