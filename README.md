# Python3 DHT scraper

## Installation

- Clone the repository.
  ```bash
  git clone https://github.com/b10n/magnet-dht
  ```

- Install the Python requirements.
  ```bash
  pip install -r requirements.txt
  ```

- Install Redis using your package manager or from source.


## Usage

The scraper is controlled via `manage.py`. To scrape the IPv6 DHT, add the `-6` flag.

```bash
python manage.py -s
```

Refer to the built-in help (`-h`) for additional options.

Collected magnets go to the Redis set `magnets`, IPv4 addresses to `ipv4`, and IPv6 addresses to `ipv6`. To count or export the collected elements, `redis-cli` can be used as usual.

```bash
redis-cli scard KEY     # count elements in KEY
redis-cli smembers KEY  # print elements in KEY
```


## Fork info

This fork adds the following features:
* IPv6 support ([BEP32](https://www.bittorrent.org/beps/bep_0032.html))
* Collecting IP addresses
* Scanning rate selection

The original README (in Chinese, memes included) is kept as [README.original.md](README.original.md).
