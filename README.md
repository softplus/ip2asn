# ip2asn

A CLI tool to look up ASN and AS Name for IP addresses.

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
