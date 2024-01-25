# Phlogiston
Project to assemble a library of application behaviors and a translator to convert them into firewall rules

This project actually serves several purposes:
1. Define a common format for describing application network behaviors that can be translated into firewall rules
2. Create a library of such behaviors
3. Create and maintain a translator for various firewall vendors

# Specification
```{
    "application":"foobar",
    "inbound":
        {
            "ip_addrs":
                {
                    "allowed":["1.1.1.0/24"],
                    "blocked":["2.2.0.0/16]
                },
            "ports":
                {
                    "allowed":["514"],
                    "blocked":["ssh","ftp","2424"]
                }
        },
    "outbound":
        {
            "allowed": ["3.3.3.3/32"],
            "blocked": ["4.4.4.0/26"]
        }
    }
```

# Desired vendor support
1. AWS
2. Cisco
3. Palo Alto
4. Azure
5. GCP
6. Fortinet
7. VyOS
8. Ubiquiti
9. OPNsense
10. pfSense
11. Untangle
12. iptables
13. pf