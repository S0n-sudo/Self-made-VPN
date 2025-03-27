THE FIRST VPN IS OUTDATED PLEASE DO NOT USE

how to use the improved one:

Prerequisites
Linux with root access
Install: sudo apt install python3 python3-pip wireguard openvpn iptables
Python libs: pip3 install aiohttp cryptography psutil pysocks netifaces

Setup
Save Script: Copy the code into vpn.py.
Optional Config: Edit vpn_config.json (e.g., password, interfaces) or use defaults.
OpenVPN Certs (if using): Place ca.crt, client.crt, client.key in the same directory.

Run

sudo python3 vpn.py
Runs a proxy server at 127.0.0.1:9050, logs to vpn.log.

Connect

App Proxy: Set SOCKS5 127.0.0.1:9050 in apps (e.g., Firefox).
System-Wide: WireGuard/OpenVPN tunnels all traffic automatically.

Stop

Ctrl+C (triggers kill switch, wipes keys).

Tips

Check vpn.log for status.
Run as service: Use systemd (see previous reply).
That’s it—secure browsing in minutes!























how to use the tor one:

Prerequisites
Linux: Root access optional for WireGuard.
Install:

sudo apt install python3 python3-pip tor
pip3 install aiohttp cryptography psutil pysocks stem

Steps
Save: Copy to tor_titan.py.

Run:
Proxy/Tor only: python3 tor_titan.py
With WireGuard: Edit tor_titan_config.json to set "use_vpn": True, then sudo python3 tor_titan.py.

Connect: Use SOCKS5 proxy 127.0.0.1:9052 (not Tor’s 9050) in apps.

Stop: Ctrl+C (triggers kill switch).


Notes

Logs in tor_titan.log.
Tor runs on 9050, proxy server on 9052.
Configurable via tor_titan_config.json.
