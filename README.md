# Suricata Rules

A collection of Suricata IDS/IPS rules and port configurations for network security monitoring and threat detection.

## Overview

This repository contains a curated set of Suricata rules and port configuration files designed to enhance network security monitoring capabilities. The rules cover various protocols, services, and security scenarios to help detect and prevent malicious network activities.

## Contents

### Port Configuration Files

- **common-ports.txt** - Standard commonly used ports across various services
- **registered-ports.txt** - IANA registered ports for well-known services
- **broadlink-ports.txt** - Ports used by Broadlink IoT devices
- **tailscale-ports** - Ports used by Tailscale VPN service
- **dynamic-ports** - Dynamically assigned ports for various services
- **private-ip.txt** - Private IP address ranges (RFC 1918)
- **tenda-mesh.txt** - Ports used by Tenda mesh networking devices

### Rule Files

- **applayer-tcpchecksum** - Application layer TCP checksum validation rules
- **safe-iana** - Safe IANA port definitions for rule filtering
- **icmp-gaming.txt** - ICMP rules for gaming traffic
- **quic.txt** - QUIC protocol detection and analysis rules

## Usage

These files can be integrated into your Suricata configuration to:

1. Define port variables and port lists for rule matching
2. Create custom rules based on specific protocols and services
3. Monitor application layer protocols
4. Identify and block potentially malicious traffic

### Basic Integration

Reference these files in your Suricata rules (`suricata.yaml`) or individual rule files:

```yaml
vars:
  port-lists:
    - common-ports.txt
    - registered-ports.txt
```

## Suricata

Suricata is a free and open source network threat detection engine. For more information, visit:
- [Suricata Official Website](https://suricata.io/)
- [Suricata Documentation](https://docs.suricata.io/)
- [Suricata GitHub Repository](https://github.com/OISF/suricata)

## License

Please check the license information in this repository for usage rights and restrictions.

## Contributing

Contributions are welcome! Feel free to:
- Submit improvements to existing rules
- Add new port configurations or rule sets
- Report issues or suggest enhancements

## Support

For questions or issues related to:
- **Suricata itself** - Visit the [Suricata Community](https://suricata.io/community/)
- **These specific rules** - Open an issue in this repository

---

Last Updated: 2026-03-20 14:05:27