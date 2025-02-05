| Sector      | VLAN | Device Type | IP Address        | Subnet Mask       | Default Gateway  |
|-------------|------|-------------|-------------------|-------------------|------------------|
| Management  | 10   | Workstation | 192.168.10.x      | 255.255.255.0     | 192.168.10.1     |
| Study       | 20   | Workstation | 192.168.20.x      | 255.255.255.0     | 192.168.20.1     |
| Production  | 30   | Workstation | 192.168.30.x      | 255.255.255.0     | 192.168.30.1     |
| Support     | 40   | Workstation | 192.168.40.x      | 255.255.255.0     | 192.168.40.1     |
| Support     | 50   | Workstation | 192.168.50.x      | 255.255.255.0     | 192.168.50.1     |
| Servers     | -    | DNS         | 192.168.60.5      | 255.255.255.0     | 192.168.60.1     |
| Servers     | -    | DHCP        | 192.168.60.10     | 255.255.255.0     | 192.168.60.1     |
| Servers     | -    | Radius      | 192.168.60.15     | 255.255.255.0     | 192.168.60.1     |
| Servers     | -    | iSCSI       | -                 | -                 | -                |
|             | 10   | Router      | G0/0.10 - 192.168.10.1 | 255.255.255.0 | -                |
|             | 20   | Router      | G0/0.20 - 192.168.20.1 | 255.255.255.0 | -                |
|             | 30   | Router      | G0/0.30 - 192.168.30.1 | 255.255.255.0 | -                |
|             | 40   | Router      | G0/0.40 - 192.168.40.1 | 255.255.255.0 | -                |
|             | 50   | Router      | G0/0.50 - 192.168.50.1 | 255.255.255.0 | -                |