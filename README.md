# ProxyList-Top-Speed

![How Proxy Servers Work](https://brightdata.com/wp-content/uploads/2024/05/How-proxy-servers-work.png)

## Overview

Welcome to **ProxyList-Top-Speed**! This repository provides a comprehensive list of proxy servers. The proxies are categorized into four types:

1. **HTTP**
2. **HTTPS**
3. **SOCKS4**
4. **SOCKS5**

## Files

The repository contains the following files:

- `proxy_http.txt` : Contains a list of HTTP proxies.
- `proxy_https.txt` : Contains a list of HTTPS proxies.
- `proxy_socks4.txt` : Contains a list of SOCKS4 proxies.
- `proxy_socks5.txt` : Contains a list of SOCKS5 proxies.

Each file is formatted as a plain text file, listing proxies in the format `[IP]:[Port]`.

## Usage

To use the proxies, you can download the respective file and integrate the proxies into your application or script. Below are the commands to download the files for different operating systems and using Python.

### Downloading using Command Line

#### Windows
```sh
curl -o proxy_http.txt https://raw.githubusercontent.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/master/proxy_http.txt
curl -o proxy_https.txt https://raw.githubusercontent.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/master/proxy_https.txt
curl -o proxy_socks4.txt https://raw.githubusercontent.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/master/proxy_socks4.txt
curl -o proxy_socks5.txt https://raw.githubusercontent.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/master/proxy_socks5.txt
```

#### macOS/Linux
```sh
wget -O proxy_http.txt https://raw.githubusercontent.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/master/proxy_http.txt
wget -O proxy_https.txt https://raw.githubusercontent.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/master/proxy_https.txt
wget -O proxy_socks4.txt https://raw.githubusercontent.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/master/proxy_socks4.txt
wget -O proxy_socks5.txt https://raw.githubusercontent.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/master/proxy_socks5.txt
```

### Downloading using Python
```python
import requests

files = {
    "proxy_http.txt": "https://raw.githubusercontent.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/master/proxy_http.txt",
    "proxy_https.txt": "https://raw.githubusercontent.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/master/proxy_https.txt",
    "proxy_socks4.txt": "https://raw.githubusercontent.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/master/proxy_socks4.txt",
    "proxy_socks5.txt": "https://raw.githubusercontent.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/master/proxy_socks5.txt"
}

for filename, url in files.items():
    response = requests.get(url)
    with open(filename, "w") as file:
        file.write(response.text)
```

## Checking Proxies

You can check the proxies using the Python tool [proxychecker](https://github.com/AmaniToamaWebDevelp1/proxychecker.git). Follow the instructions in the tool's repository to verify the proxies provided in this project.

![ProxyChecker Tool](https://github.com/AmaniToamaWebDevelp1/proxyList-Top-Speed/blob/master/12Capture.PNG)

## Contribution

Contributions are welcome! If you have proxies to add or updates to existing proxies, please fork the repository and submit a pull request.

## License

This project is licensed under the GPL-3.0 License - see the [LICENSE](LICENSE) file for details.

## Contact

For more information, feel free to contact the maintainer at [amanitoama570@gmail.com](mailto:amanitoama570@gmail.com).

---

Happy Proxying!
