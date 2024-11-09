# proxyList-Top-Speed

## Overview
**proxyList-Top-Speed** provides a list of high-speed, free, public, forward proxy servers, updated daily.

![Proxy List](https://brightdata.com/wp-content/uploads/2024/05/How-proxy-servers-work.png)

## Getting Started

### Download
To download and save the proxy list to a local file `proxyList-Top-Speed.txt` with the format `IP:PORT`, use the following command:
```bash
curl -sSf "https://raw.githubusercontent.com/Amani-Toam/proxyList-Top-Speed/master/proxyList-Top-Speed-raw.txt" > proxyList-Top-Speed.txt
```

### File Format

#### proxyList-Top-Speed.txt
```plaintext
IP:Port | Country | Anonymity | Type | Google Passed

Example:
200.2.125.90:8080 | AR | N | S! | +

Legend:
1. IP address
2. Port number
3. Country code (ISO 3166-1 alpha-2)
4. Anonymity 
   - N: No anonymity
   - A: Anonymity
   - H: High anonymity
5. Type
   - HTTP
   - S: HTTP/HTTPS
   - !: Incoming IP differs from outgoing IP
6. Google passed
   - +: Yes
   - -: No
```

#### proxyList-Top-Speed-status.txt
```plaintext
IP:Port | Status

Example:
200.2.125.90:8080 | success

Legend:
1. IP address
2. Status
   - success: Low latency (0-9 seconds)
   - failure: High latency (10+ seconds)
```

## API Usage

### PubProxy API
[PubProxy](http://pubproxy.com/) offers a free, robust API to narrow down the proxy to your desired specification. Here are some example parameters and usage:

```plaintext
Parameters:
- FORMAT: json, txt (Output format)
- LEVEL: anonymous, elite (Anonymity level)
- TYPE: http, socks4, socks5 (Proxy protocol)
- LAST_CHECK: 1-1000 (Last check time in minutes)
- LIMIT: 1-20 (Number of proxy results)
- COUNTRY: US,CA,... (Country of the proxy)
- NOT_COUNTRY: MX,CA,... (Exclude proxy countries)
- PORT: Number (Specify port number)
- GOOGLE: Boolean (Google passed proxies)
- HTTPS: Boolean (Supports HTTPS request)
- GET: Boolean (Supports GET request)
- POST: Boolean (Supports POST request)
- USER_AGENT: Boolean (Supports USER_AGENT request)
- COOKIES: Boolean (Supports COOKIES request)
- REFERER: Boolean (Supports REFERER request)

Examples:
# Retrieve one (1) socks5 proxy.
curl "http://pubproxy.com/api/proxy?limit=1&format=txt&type=socks5"

# Retrieve two (2) HTTP proxies from the US that support HTTPS.
curl "http://pubproxy.com/api/proxy?limit=2&format=txt&http=true&country=US&type=http"
```

## Test Proxy List

Test the proxy list with my other tool [ProxyChecker](https://github.com/AmaniToamaWebDevelp1/proxychecker.git):
- A fast and efficient command-line tool for validating proxies.
- Designed for cybersecurity professionals, developers, and web scrapers.
- Supports both single proxy checks and bulk validation from files and URLs.
- Compatible across HTTP, HTTPS, and SOCKS protocols.

## References
- [ISO 3166-1 alpha-2 country code](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)
- [Google passed proxy](https://www.my-proxy.com/blog/google-proxies-dead)

## :star: Credits
Proxy server data courtesy of:
- [Proxyspy](http://spys.one/en/)
- [PubProxy](http://pubproxy.com/)

---

**Amani Toama**
