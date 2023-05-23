

# Kumpulan Wazuh Detection Rules

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/TrueMelody/Kumpulan-Rules-Wazuh">
    <img src="images/wazuh_logo.png" alt="Logo">
  </a>

  <h3 align="center">Kumpulan Wazuh Detection Rules</h3>

  <p align="center">
    Rules pada Wazuh merupakan seperangkat aturan yang digunakan oleh platform Wazuh dalam mendeteksi aktivitas atau kejadian yang mencurigakan atau berbahaya dalam suatu sistem atau jaringan. Rules ini dirancang untuk mengidentifikasi suatu tanda-tanda adanya serangan, Security threats, atau abnormal behaviour yang dapat menunjukkan adanya intrusion pada suatu jaringan atau sistem. Repositori ini bertujuan memberikan suatu rules wazuh yang lebih akurat, deskriptif, dan beragam, yang diperoleh dari berbagai sumber yang terpercaya.
    <br />
    <br />
    <a href="https://documentation.wazuh.com/current/index.html">Wazuh Docs</a>
    <br>
    <a href="https://belvasgg.medium.com/">My Blog</a>
  </p>
</div>


<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-this-repo">About This Repo</a>
      <ul>
        <li><a href="#supported-rules-and-integrations">Supported Rules and Integrations</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About This Repo

Tujuan dari repositori ini adalah menyediakan ruleset wazuh yang lebih akurat, deskriptif dari berbagai sumber yang terpercaya.

Here's why:
* Detection rule merupakan hal yang cukup rumit, dan kami percaya bahwa setiap orang harus memiliki akses ke wazuh ruleset yang kuat dan terpercaya.
* Wazuh berfungsi sebagai EDR (Endpoint Detection and Response) yang cukup baik, namun ruleset bawaannya terbilang kurang baikd dan kurang ketat. Maka dari itu, tujuan dari repositori ruleset wazuh ini adalah agar dapat diimplementasikan oleh komunitas dan diperluas ketika ancaman baru muncul kepermukaan.
* Cybersecurity is hard enough, let's work together :smile:


<p align="right">(<a href="#readme-top">back to top</a>)</p>


### Rules dan Integrations yang di Support

Berikut ini adalah rules dan integrasi yang saat ini terdapat dalam repositori ini. Integrasi seperti Office365, Trend Micro, dan sebagainya akan memiliki skrip yang disediakan dalam foldernya masing-masing untuk digunakan. Anda dapat dengan bebas memperluas skrip-skrip ini dan berkontribusi kembali ke repositori ini.

* [Sysmon for Windows](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Windows_Sysmon)
* [Sysmon for Linux](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Sysmon%20Linux)
* [Office365](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/main/Office%20365)
* [Microsoft Defender](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Office%20Defender)
* [Sophos](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Sophos)
* [MISP](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/MISP)
* [Osquery](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Osquery)
* [Yara](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Yara)
* [Suricata](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Suricata)
* [Packetbeat](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Packetbeat)
* [Falco](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Falco)
* [Modsecurity](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Modsecurity)
* [F-Secure](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/F-Secure)
* [Domain Stats](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Domain%20Stats)
* [Snyk](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Snyk)
* [Autoruns](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Windows%20Autoruns)
* [Sigcheck](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Windows%20Sysinternals%20Sigcheck)
* [Powershell](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Windows%20Powershell)
* [Crowdstrike](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Crowdstrike)
* [Alienvault](https://github.com/TrueMelody/Kumpulan-Rules-Wazuh/tree/main/Domain%20Stats)
* Tessian - WIP

<!-- GETTING STARTED -->
## Getting Started

Anda bebas untuk mengimplementasikan semua ruleset yang terdapat dalam repositori ini, atau memilih ruleset yang sesuai dengan kebutuhan Anda. Silakan lihat bagian Instalasi di bawah ini untuk mendapatkan script bash yang dapat dijalankan pada Wazuh Manager Anda agar aturan-aturan ini segera bekerja dengan baik!

### Prerequisites

Wazuh-Manager Version 4.x Required.

[Wazuh Install Docs](https://documentation.wazuh.com/current/index.html)

### Installation

> :warning: **USE AT OWN RISK**: If you already have custom rules built out, there is a good chance duplicate Rule IDs will exists. This will casue the Wazuh-Manager service to fail! Ensure there are no conflicting Rule IDs and your custom rules are backed up prior to running the wazuh_rules.sh script!


1. Harus menjadi Root User
2. Jalankan Script ini 
   ```sh
   curl -so ~/wazuh_rules.sh https://raw.githubusercontent.com/TrueMelody/Kumpulan-Rules-Wazuh/main/wazuh_rules.sh && bash ~/wazuh_rules.sh
   ```

![Alt Text](https://github.com/socfortress/Wazuh-Rules/blob/main/images/run%20install.gif)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
<br>
<br>
<br>
<p>Credit : SOCFORTRESS (INDONESIAN TRANSLATION)</p>

