Setup and Running

Install Dependencies:

pip install requests beautifulsoup4 aiohttp cryptography argon2-cffi pqcrypto stegano pillow backoff

Prepare Image:
Place base_image.png (or let it generate a 1024x1024 fallback).

Set Password:
export
IP_CHANGER_PASS="YourSuperSecurePass123!"

run:
python ip_changer.py

Update Checksum: 
Replace YOUR_CRITICAL_CHECKSUM with:

critical_code = (derive_key.__code__.co_code + encrypt_proxy.__code__.co_code + change_ip.__code__.co_code)
print(hashlib.sha256(critical_code).hexdigest())
