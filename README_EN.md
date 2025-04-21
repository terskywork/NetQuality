<p align="center">
<img src="https://hits.xykt.de/net.svg?action=view&count_bg=%2379C83D&title_bg=%23555555&title=Runs&edge_flat=false"/> 
<img src="https://hits.xykt.de/net_github.svg?action=hit&count_bg=%233DC8C0&title_bg=%23555555&title=Visits&edge_flat=false"/> 
<a href="/LICENSE"><img src="https://img.shields.io/badge/License-AGPL%20v3-blue.svg" alt="license" /></a>  
</p>

## Network Quality Check Script  -  [网络质量体检脚本 (CN)](https://github.com/xykt/NetQuality)

**Supported OS/Platform: Ubuntu | Debian | Linux Mint | Fedora | Red Hat Enterprise Linux (RHEL) | CentOS | Arch Linux | Manjaro | Alpine Linux | AlmaLinux | Rocky Linux | macOS | Anolis OS | Alibaba Cloud Linux | SUSE Linux | openSUSE | Void Linux**

- Bilingual support: English & Chinese
- Supports IPv4/IPv6 dual-stack queries
- Well-formatted output for clear and concise display, optimized for screenshots
- Seven key modules: BGP information, local policy, access information, three-network TCP large packet latency, three-network return routing, domestic speed test, and international interconnection
- Base data sourced from *BGP.TOOLS* and *BGP.HE.NET* databases
- Intuitive display of upstream and access information
- Return latency tests for China Mainland’s 31 provinces/cities/autonomous regions via China Telecom, China Unicom, and China Mobile
- Speed test for China Mainland’s three major ISPs (including the Greater Bay Area) based on *SPEEDTEST.NET*
- Global speed and latency tests across five continents
- Flexible test modes: latency mode, low data mode, selective section skipping
- JSON output for big data analysis

##### Screenshots

| IPv4 Test Result | IPv6 Test Result |
| ---------------- | ---------------- |
|![IPv4](https://github.com/xykt/NetQuality/raw/main/res/v4_en.png)|![IPv6](https://github.com/xykt/NetQuality/raw/main/res/v6_en.png)|

| Latency Mode Test Result | Full Route Mode Test Result |
| ---------------- | ---------------- |
|![Ping](https://github.com/xykt/NetQuality/raw/main/res/ping_en.png)|![Route](https://github.com/xykt/NetQuality/raw/main/res/route_v4.png)|

## Usage

### Easy Mode: Run with Interactive Interface

![Net](https://github.com/xykt/ScriptMenu/raw/main/res/Net_EN.png)

````bash
bash <(curl -Ls Check.Place) -EN
````

### Advanced Mode: Run with Parameters

![Help](https://github.com/xykt/NetQuality/raw/main/res/help.png)

##### Default dual-stack detection (Either):

```bash
bash <(curl -Ls Net.Check.Place) -E
bash <(curl -Ls Net.Check.Place) -l en
```

##### IPv4-only test:

```bash
bash <(curl -Ls Net.Check.Place) -E4
```

##### IPv6-only test:

```bash
bash <(curl -Ls Net.Check.Place) -E6
```

##### Latency mode:

```bash
bash <(curl -Ls Net.Check.Place) -EP
```

##### Low data mode:

```bash
bash <(curl -Ls Net.Check.Place) -EL
```

##### Full route mode (TCP result in Chinese):

```bash
bash <(curl -Ls Net.Check.Place) -E -R [Province]
```
Test Beijing & Shanghai & Guangdong by default:
```bash
bash <(curl -Ls Net.Check.Place) -E -R
```
Specify parameters to detect the corresponding province (Any of the following):
```bash
bash <(curl -Ls Net.Check.Place) -E -R 桂
bash <(curl -Ls Net.Check.Place) -E -R 广西
bash <(curl -Ls Net.Check.Place) -E -R 广西壮族自治区
bash <(curl -Ls Net.Check.Place) -E -R GX
bash <(curl -Ls Net.Check.Place) -E -R gx
```

##### Skip specific sections:

```bash
bash <(curl -Ls Net.Check.Place) -E -S 1234567
```

##### Bilingual support:

```bash
bash <(curl -Ls Net.Check.Place) -l cn|en
```

##### JSON output ([Example Output](https://github.com/xykt/NetQuality/blob/main/res/output.json)):

```bash
bash <(curl -Ls Net.Check.Place) -Ej
```

##### Skip checking OS and dependencies:

```bash
bash <(curl -Ls Net.Check.Place) -En
```

##### Auto-install dependencies:

```bash
bash <(curl -Ls Net.Check.Place) -Ey
```

##### Display full IP addresses in the report:

```bash
bash <(curl -Ls Net.Check.Place) -Ef
```

## Script Updates

2025/04/21 22:15 Collapse routing duplicate information for full routing mode

2025/04/21 00:00 Fix macOS compatibility issues and improve script robustness

2025/04/20 21:00 Fixed connectivity issues with CN IPs

2025/03/28 00:50 Add -R Full Route Mode, add international delay test to Low Data Mode, fix bugs

2025/03/13 22:40 Add -n for no checking OS & dependencies

2025/03/12 17:00 Script Released

## Contributions

**Server Sponsor:**

| Sponsor | Logo | Link | 
| - | - | - | 
| V.PS | ![vps_logo](https://raw.githubusercontent.com/xykt/NetQuality/main/res/sponsor/logo_vps.png) | [https://v.ps](https://v.ps)| 
| BAGE | ![bage_logo](https://raw.githubusercontent.com/xykt/NetQuality/main/res/sponsor/logo_bage.png) | [https://bagevm.com](https://bagevm.com)|
| LisaHost | ![lisa_logo](https://raw.githubusercontent.com/xykt/NetQuality/main/res/sponsor/logo_lisa.png) | [https://lisahost.com](https://lisahost.com)|
| DreamCloud | ![dreamcloud_logo](https://raw.githubusercontent.com/xykt/NetQuality/main/res/sponsor/logo_dreamcloud.png) | [https://as211392.com/](https://as211392.com/)|

**Only accepting merchants with long-term stable operations and good reputation*

**Acknowledgments:**

- Special thanks to [GlobalSign@Nodeseek](https://www.nodeseek.com/space/5813#/general) for providing a stable and reliable three-network test address, laying a solid foundation for one of the script's most important features.

- Thanks to [Sherlock@Nodeseek](https://www.nodeseek.com/space/13352#/general) for valuable suggestions on functionality and aesthetics.

- Thanks to [酒神@Nodeseek](https://www.nodeseek.com/space/9#/general) for technical support and valuable feedback.

- Thanks to Si for important recommendations on script functionality and formatting.

- Thanks to Kakan for providing valuable reference suggestions.


**Stars History:**

![Stargazers over time](https://starchart.cc/xykt/NetQuality.svg?background=%23FFFFFF&axis=%23333333&line=%2377ff77)

