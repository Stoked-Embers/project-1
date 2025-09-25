# DESIGN.md

## overview
Demonstrates a simple Node.js app deployed on an AWS EC2 instance. The simple REST API converts lbs to kg and retuns in a 
json format.

Design prioritizes:
 - key pairs and Security Groups with least privilege
 - JSON shape, numeric handling, error codes
 - service managed by systemd
 - README clarity, curl examples

---

## system architecture
 - AWS Ubuntu 20.04LTS t2 micro
 - Security:
      - SSH resctricted to my IP
      - HTTP (8080) open for testing
 - Simple express server exposing /convert
 - systemd unit file ensures bootup on start
<img width="1595" height="1649" alt="image" src="https://github.com/user-attachments/assets/aadb1342-5032-48ef-9c14-5f96f8014bf8" />

## error handling
 - Missing lbs: return {"error":"Query param lbs is required and must be a number"}
 - Non-numeric lbs: same error.

<img width="1101" height="303" alt="image" src="https://github.com/user-attachments/assets/c56f64cf-e9be-4910-8954-687549f4db7e" />

## Service reliability
 - starts on boot
 - logs accessable with journalctl -u nodeapp
 - verified by rebooting

<img width="1256" height="342" alt="image" src="https://github.com/user-attachments/assets/f6f0181b-ca24-41db-b63d-1d44b1497f31" />
