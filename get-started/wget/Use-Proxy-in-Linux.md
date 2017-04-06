# Configure Proxy for Wget in Linux

> Created by Fisher at 19:02 on 2017-04-06.

Sometimes using a proxy will be helpful and here are several ways to use proxy in `wget`.

Here we suppose your proxy address/ip is `127.0.0.1` and port is `1080`.
You can set up

## Temperately Usage

```bash
wget ... -e use_proxy=yes -e http_proxy=127.0.0.1:1080 -e https_proxy=127.0.0.1:1080 ...
```

Add alias in your ~/.bashrc file

```
alias wget-proxy="wget -e use_proxy=yes -e http_proxy=127.0.0.1:1080 -e https_proxy=127.0.0.1:1080";
```

## Edit either `/etc/wgetrc` or `~/.wgetrc`.

```bash
# You can set the default proxies for Wget to use for http, https, and ftp.
# They will override the value in the environment.
http_proxy = http://127.0.0.1:1080/
https_proxy = http://127.0.0.1:1080/
ftp_proxy = http://127.0.0.1:1080/

# If you do not want to use proxy at all, set this to off.
use_proxy = on
```

## Uses Environment Variables

```bash
export http_proxy=http://ip-of-proxy-server:port/
export https_proxy=$http_proxy
export ftp_proxy=$http_proxy
export dns_proxy=$http_proxy
export rsync_proxy=$http_proxy
export no_proxy="localhost,127.0.0.1,localaddress,.localdomain.com"
```


## References

- Stackoverflow: [Setting Up Proxy for Wget][stackoverflow-setting-proxy-in-wget].



[stackoverflow-setting-proxy-in-wget]: http://stackoverflow.com/questions/11211705/setting-proxy-in-wget
