# Wireshark DNS Investigation Lab

A comprehensive hands-on laboratory for learning DNS protocol analysis, troubleshooting, and security investigation using Wireshark.

## Lab Overview

This lab provides practical exercises for understanding DNS communication, identifying anomalies, and investigating security-related DNS issues. Participants will learn to:

- Capture and analyze DNS traffic
- Identify DNS query and response patterns
- Detect DNS spoofing and cache poisoning attempts
- Investigate DNS tunneling and exfiltration
- Troubleshoot DNS resolution issues
- Recognize indicators of compromise (IoCs) in DNS logs

## Prerequisites

- Wireshark (version 3.x or later) - [Download](https://www.wireshark.org/download/)
- Basic understanding of DNS protocol
- Basic networking knowledge (TCP/IP)
- A lab environment or sample pcap files for analysis

## Repository Structure

```
wireshark-dns-lab/
├── README.md                    # This file
├── docs/                        # Documentation and guides
│   ├── dns-basics.md           # DNS protocol overview
│   ├── wireshark-setup.md      # Wireshark installation and configuration
│   └── analysis-techniques.md  # DNS analysis methodologies
├── exercises/                   # Lab exercises
│   ├── exercise-1-basic-dns/   # Basic DNS queries and responses
│   ├── exercise-2-dns-resolution/
│   ├── exercise-3-dns-anomalies/
│   ├── exercise-4-dns-spoofing/
│   └── exercise-5-dns-security/
├── pcap-files/                 # Sample packet capture files
│   ├── normal-dns-traffic.pcap
│   ├── dns-spoofing-attempt.pcap
│   ├── dns-tunneling.pcap
│   └── dns-exfiltration.pcap
├── solutions/                   # Exercise solutions and explanations
│   ├── solution-1.md
│   ├── solution-2.md
│   └── ...
├── resources/                   # Additional resources
│   ├── wireshark-filters.txt   # Useful display filters
│   ├── dns-query-types.md      # DNS query type reference
│   └── troubleshooting-guide.md
└── LICENSE                      # License information

```

## Quick Start

1. **Install Wireshark**: Follow the [setup guide](docs/wireshark-setup.md)
2. **Learn DNS Basics**: Read [DNS Basics](docs/dns-basics.md)
3. **Start with Exercise 1**: Begin with [Basic DNS Queries](exercises/exercise-1-basic-dns/README.md)
4. **Progress Through Exercises**: Complete exercises in order for progressive learning
5. **Review Solutions**: Check [solutions](solutions/) to verify your analysis

## Lab Exercises

### Exercise 1: Basic DNS Queries and Responses
Learn to identify and analyze standard DNS queries and responses.

### Exercise 2: DNS Resolution Process
Understand the full DNS resolution process from query to answer.

### Exercise 3: DNS Anomalies
Identify unusual DNS patterns and potential issues.

### Exercise 4: DNS Spoofing and Cache Poisoning
Detect DNS spoofing attempts and cache poisoning attacks.

### Exercise 5: DNS Security Investigation
Investigate DNS tunneling and data exfiltration attempts.

## Useful Wireshark Display Filters

```
dns              # Show all DNS traffic
dns.qry.type==A  # Show only A record queries
dns.flags.rcode==3  # Show NXDOMAIN responses
dns.flags.aa==1  # Show authoritative answers
```

For more filters, see [Wireshark Filters Reference](resources/wireshark-filters.txt)

## Key DNS Concepts

- **Query (QR=0)**: Client asking for information
- **Response (QR=1)**: Server providing answer
- **Recursive Query**: Client requests full resolution
- **Iterative Query**: Client accepts referral to another server
- **Authoritative Answer (AA)**: Server is authoritative for the domain
- **Truncated (TC)**: Message was truncated

## Common DNS Record Types

| Type | Purpose |
|------|---------|
| A | IPv4 address |
| AAAA | IPv6 address |
| MX | Mail exchange server |
| CNAME | Canonical name (alias) |
| NS | Nameserver |
| SOA | Start of authority |
| TXT | Text record |
| PTR | Reverse DNS lookup |

## Requirements

- Wireshark 3.x or later
- Administrator/sudo privileges for packet capture
- Sample pcap files (included in repository)
- Text editor for notes
- Optional: Python 3.x for advanced analysis scripts

## Tips for Success

1. **Start Simple**: Begin with basic DNS traffic before complex scenarios
2. **Use Filters**: Master Wireshark filters to focus on relevant packets
3. **Document Findings**: Take notes on observations and patterns
4. **Cross-Reference**: Use DNS references to understand query types and response codes
5. **Practice**: Repeat exercises with different pcap files
6. **Analyze Real Traffic**: Capture your own DNS traffic for additional practice

## Troubleshooting

If you encounter issues, refer to the Troubleshooting Guide or check the FAQ section below.

## FAQ

**Q: Can I use Wireshark on Linux/Mac/Windows?**
A: Yes, Wireshark is cross-platform and works on all three operating systems.

**Q: Do I need administrative privileges?**
A: Yes, to capture live traffic you'll need administrator/sudo access.

**Q: Are there sample pcap files included?**
A: Sample pcap files will be added to the `pcap-files/` directory.

**Q: Can I use my own pcap files?**
A: Absolutely! The techniques apply to any DNS traffic capture.

## Contributing

Contributions are welcome! To contribute:

1. Fork the repository
2. Create a feature branch
3. Add improvements, exercises, or fixes
4. Submit a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Resources

- [Wireshark Official Documentation](https://www.wireshark.org/docs/)
- [DNS RFC 1035](https://tools.ietf.org/html/rfc1035)
- [DNS Security Extensions (DNSSEC)](https://tools.ietf.org/html/rfc4033)
- [OWASP DNS Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/DNS_Security_Cheat_Sheet.html)

## Support

For questions or issues, please:
1. Review existing documentation
2. Check [Issues](../../issues)
3. Create a new [Issue](../../issues/new) with detailed information

---

**Last Updated**: 2026-05-18  
**Version**: 1.0.0
