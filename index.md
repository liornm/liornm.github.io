<link rel="shortcut icon" type="image/png" href="img/face_blur_circle.png?">

## <img src="img/Bluetooth.svg" alt="drawing" width="11"/> Breaking the Bluetooth Pairing

The pairing protocol is the process of connection establishment in Bluetooth. This process supplies the ground for all of the security and privacy features provided by Bluetooth. Failing to secure this process compromises the entire Bluetooth session.

Based on newly discovered protocol design flaws ([CVE-2018-5383](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-5383)), we have developed a technique for attacking the Bluetooth pairing protocol by manipulating specific protocol messages. The attack can be used in order to evesdrop to any Bluetooth session and forge messages without user awareness.

The [paper](https://www.springerprofessional.de/en/breaking-the-bluetooth-pairing-the-fixed-coordinate-invalid-curv/17554980) published at the Selected Areas in Cryptography (SAC) '19 conference.

Popular [summary](https://hackernoon.com/bluetooth-hacking-cheating-in-elliptic-curve-billiards-c092fdf70aae) of our attack by Tal Be'ery.

The work is part of my thesis at the Technion - Israel Institute of Technology.

<p align="center">
<img src="img/bt_ppls.png" alt="drawing" width="200"/></p>

### Bluetooth Standard Change
As a result of our publication, the Bluetooth Special Intrest Group released a change to the Bluetooth Core Specification (the Bluetooth standard) denoted by ``Erratum 10734: Pairing Updates``, see the complete change [here](https://www.bluetooth.org/docman/handlers/downloaddoc.ashx?doc_id=447440).

### Affected Operating Systems

| Vendor        | Products                          | Ref                                                             |
| ------------- |-----------------------------------|-----------------------------------------------------------------|
| Apple  | macOS High Sierra 10.13.6 and below             | [link](https://support.apple.com/en-us/HT208937)                |
| Apple  | iOS 11.4 and below                              | [link](https://support.apple.com/en-us/HT208848)                |
| Google | Android (AOSP) before Security Patch 2018-06-01 | [link](https://source.android.com/security/bulletin/2018-06-01) |

### Affected Wireless Chips

| Vendor        | Products       | Ref   |
| ------------- |-------------| -----|
| Intel | Dual Band Wireless-AC 3160, Wireless-N 7260, Dual Band Wireless-N 7260, Dual Band Wireless-AC 7260, Dual Band Wireless-AC 3165, Dual Band Wireless-AC 3168, ... | [link](https://www.intel.com/content/www/us/en/security-center/advisory/intel-sa-00128.html) |
| Qualcomm | AR9344, MDM9206, MDM9607, MDM9635M, MDM9640, MDM9650, MSM8909W, MSM8996AU, QCA6174A, QCA6564, QCA6574, QCA6574AU, QCA9377, QCA9379, QCA9886, ... | [link](https://www.qualcomm.com/company/product-security/bulletins/archives/august-2018#_CVE-2018-5383) |
| Broadcom | BCM4339, BCM4358, ... | No official publication. |

### In the News
* [Forbes](https://www.forbes.com/sites/thomasbrewster/2018/07/24/bluetooth-hack-warning-for-iphone-android-and-windows/?sh=7fb9884f7d73)
* [The Register](https://www.theregister.com/2018/07/24/bluetooth_cryptography_bug/)
* [Wired](https://www.wired.com/story/decade-old-bluetooth-flaw-leaves-countless-devices-exposed/)
* [ZDNet](https://www.zdnet.com/article/bluetooth-security-flaw-could-allow-nearby-attacker-to-grab-your-private-data/)
* [Schneier on Security](https://www.schneier.com/blog/archives/2018/07/major_bluetooth.html)
* [Hindustan Times](https://tech.hindustantimes.com/tech/news/bluetooth-vulnerability-puts-millions-of-devices-at-risk-here-s-what-you-should-do-story-xraie3IEBN39YMENA9Y2ZI.html)
* [MyBroadband](https://mybroadband.co.za/news/security/269759-bluetooth-bug-lets-hackers-snoop-on-data-exchanged-between-devices.html)
* [ZDNet (French)](https://www.zdnet.fr/actualites/bluetooth-une-faille-pour-acceder-aux-donnees-en-theorie-39871655.htm)
* [Connect (German)](https://www.zdnet.fr/actualites/bluetooth-une-faille-pour-acceder-aux-donnees-en-theorie-39871655.htm)
* [SecurityLab.ru (Russian)](https://www.securitylab.ru/news/494601.php)
* [Security Next (Japanese)](https://www.security-next.com/096040)
* [Ynet (Hebrew)](https://www.ynet.co.il/articles/0,7340,L-5316453,00.html)
* [Israel HaYom (Hebrew)](https://www.israelhayom.co.il/article/574289)
