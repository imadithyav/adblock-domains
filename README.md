# adblock-hosts
Major hosts files are merged into a single file
# configuration profiles 
## For Apple Ecosystem
To block ads across your Apple ecosystem (iOS, iPadOS, and macOS) using DNS over HTTPS (DoH) via RethinkDNS, you are essentially routing your internet traffic through a "filter" that ignores requests from known ad servers.
### Implementation Steps
#### Configure your Resolver: Go to the RethinkDNS website to select which blocklists you want (e.g., OISD, StevenBlack).
Get your Unique URL: Once configured, RethinkDNS provides a unique DoH URL.
#### Deploy via Profile (Recommended):
iOS/iPadOS/macOS: Adding DNS Profile using the Apple Configurator containing your DoH URL.
Install this in Settings > General > VPN & Device Management.
#### Video Tutorial
Link for iPad OS and iOS: https://youtu.be/kNBsxAnvLPk
Link for macOS: https://youtu.be/RargMv9_sxM.
## Why use RethinkDNS over others?
Because RethinkDNS offers a customizable, server-side blocking engine, you don't need to keep a heavy app running in the background to filter traffic; the DNS server does the heavy lifting for you.
### How it Works
Traditional DNS sends your requests in plain text, making them easy to track or spoof. DoH encrypts these requests. When you use RethinkDNS, every time an app or website tries to load an ad (like ads.google.com), the DNS server simply returns a "not found" result, preventing the ad from ever downloading.

