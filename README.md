# Cloudflare Preferred IPs

Automatically measured every six hours with CFData-WEB.

- `cm.txt`: edgetunnel preferred-IP API, one `IP:443#remark` per line.
- `results.csv`: measured latency, download speed and datacenter.
- `status.json`: last successful measurement time and result count.

Use this address in edgetunnel's subscription-interface API URL:

```text
https://raw.githubusercontent.com/lolo810/cfdata-results/main/cm.txt
```

Default port: `443`. Leave **Use preferred IPs as PROXYIP** unchecked.
These are Cloudflare entry addresses, not verified proxy exit addresses.

Results reflect the measuring network. Only addresses that pass real download
tests are published. Failed or empty runs do not replace the previous results.
The fixed files contain the latest successful run; Git history retains past
versions. No credentials, configuration files or raw logs are published.
