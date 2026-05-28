# OnionHop Bridges Collector

Automatically collects, validates and archives Tor bridges for the
[OnionHop](https://github.com/center2055/OnionHop) app. A GitHub Action runs
hourly to fetch fresh bridges from the official Tor Project and community
sources, then TCP/TLS-tests them.

_Last updated: 2026-05-28 23:27 UTC_

## Lists

| Transport | Tested & Active (IPv4) | Fresh 72h (IPv4) | Full Archive (IPv4) | Full Archive (IPv6) |
| :--- | :--- | :--- | :--- | :--- |
| **obfs4** | [obfs4_tested.txt](https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/obfs4_tested.txt) (255) | [obfs4_72h.txt](https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/obfs4_72h.txt) (481) | [obfs4.txt](https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/obfs4.txt) (481) | [obfs4_ipv6.txt](https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/obfs4_ipv6.txt) (262) |
| **webtunnel** | [webtunnel_tested.txt](https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/webtunnel_tested.txt) (92) | [webtunnel_72h.txt](https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/webtunnel_72h.txt) (170) | [webtunnel.txt](https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/webtunnel.txt) (170) | [webtunnel_ipv6.txt](https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/webtunnel_ipv6.txt) (171) |
| **vanilla** | [vanilla_tested.txt](https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/vanilla_tested.txt) (193) | [vanilla_72h.txt](https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/vanilla_72h.txt) (426) | [vanilla.txt](https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/vanilla.txt) (426) | [vanilla_ipv6.txt](https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/vanilla_ipv6.txt) (30) |

IPv6 variants exist for every list (e.g. `obfs4_ipv6_tested.txt`,
`obfs4_ipv6_72h.txt`). Note: IPv6 `*_tested` lists may be empty because CI
runners often lack IPv6 connectivity — prefer IPv4 where possible.

## Consuming these lists

Fetch the raw files directly, e.g.:

```
https://raw.githubusercontent.com/center2055/OnionHop-Bridges-Collector/main/bridge/obfs4_tested.txt
```

For censorship resilience, mirror the same paths behind GitHub Pages, a CDN,
and/or a self-hosted domain, and try them in order. OnionHop's in-app
**Bridge Scanner** reads these files and TCP-pings them so users can pick the
bridges that actually work in their region.

## Sources

- Official Tor BridgeDB: `https://bridges.torproject.org`
- Community seed: [Delta-Kronecker/Tor-Bridges-Collector](https://github.com/Delta-Kronecker/Tor-Bridges-Collector)

## Disclaimer

For educational and circumvention purposes. Use bridges responsibly and in
accordance with your local laws.
