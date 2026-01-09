# ip2asn

A CLI tool to look up ASN and AS Name for IP addresses.

Copyright (c) 2026 John Mueller

https://github.com/softplus/ip2asn

## Features
- Extracts IPv4 and IPv6 addresses from files or standard input.
- Uses Team Cymru Bulk Whois for fast, free lookups.
- Local SQLite cache at `~/.cache/ip2asn.db`.
- 24-hour cache TTL.
- No root required.

## Installation
Ensure you have Python 3 installed.

```bash
# Make the script executable
chmod +x ip2asn
```

## Usage

### Pipe input
```bash
cat sample.txt | ./ip2asn
```

### Positional arguments
```bash
./ip2asn 8.8.8.8 1.1.1.1
```

### URL arguments
```bash
./ip2asn https://www.egloff.eu/qralocator/viewlogqralocator.php
```

### File arguments
```bash
./ip2asn sample.txt long-sample.txt
```

### Output format
```
IPADDRESS | ASN | ASNAME
66.249.73.1 | 15169 | GOOGLE, US
```

## Testing
Run the provided test files:
```bash
./ip2asn sample.txt
./ip2asn long-sample.txt
```

## License
MIT License - see [LICENSE](LICENSE) for details.
