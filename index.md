## <img src="img/Bluetooth.svg" alt="drawing" width="11"/> Breaking the Bluetooth Pairing

The pairing protocol is the process of connection establishment in Bluetooth. This process supplies the ground for all of the security and privacy features provided by Bluetooth. Failing to secure this process compromises the entire Bluetooth session.

In my research I had devwloped a technique for attacking the Bluetooth pairing protocol by manipulating specific messages, without being detected by the victim devices. This attack relies on a newly discovered protocol design flaws. Using this attack, one can exploit these flaws in order to reveal the encryption keys of the victim devices and use it  to decrypt and forge data without user awareness.

The [paper](https://www.springerprofessional.de/en/breaking-the-bluetooth-pairing-the-fixed-coordinate-invalid-curv/17554980) was published in Selected Areas in Cryptography (SAC) '19 conference.

### Bluetooth SIG Standard Change
Due to our publication the Bluetooth Special Intrest Group released a change to the Bluetooth Core Specification (the Bluetooth standard) denoted by ``Erratum 10734: Pairing
Updates``, see the complete change [here](https://www.bluetooth.org/docman/handlers/downloaddoc.ashx?doc_id=447440).

### Affected Operating Systems

| Vendor        | Products                          | Ref                                                             |
| ------------- |-----------------------------------|-----------------------------------------------------------------|
| Apple  | macOS High Sierra 10.13.6 and below      | [link](https://support.apple.com/en-us/HT208937)                |
| Apple  | iOS 11.4 and below                       | [link](https://support.apple.com/en-us/HT208848)                |
| Google | Android (AOSP) Security Patch 2018-06-01 | [link](https://source.android.com/security/bulletin/2018-06-01) |

### Affected Wireless Chips

| Vendor        | Products       | Ref   |
| ------------- |-------------| -----|
| Intel | Intel® Dual Band Wireless-AC 3160, Intel® Wireless-N 7260, Intel® Dual Band Wireless-N 7260, Intel® Dual Band Wireless-AC 7260, Intel® Dual Band Wireless-AC 3165, Intel® Dual Band Wireless-AC 3168, Intel® Wireless-N 7265, Intel® Dual Band Wireless-N 7265, Intel® Dual Band Wireless-AC 7265, Intel® Tri-Band Wireless-AC 17265, Intel® Dual Band Wireless-AC 8260, Intel® Tri-Band Wireless-AC 18260, Intel® Dual Band Wireless-AC 8265, Intel® Tri-Band Wireless-AC 18265, Intel® Wireless-AC 9260, Intel® Wireless-AC 9461, Intel® Wireless-AC 9462, and Intel® Wireless-AC 9560 | [link](https://www.intel.com/content/www/us/en/security-center/advisory/intel-sa-00128.html) |
| Qualcomm | AR9344, MDM9206, MDM9607, MDM9635M, MDM9640, MDM9650, MSM8909W, MSM8996AU, QCA6174A, QCA6564, QCA6574, QCA6574AU, QCA9377, QCA9379, QCA9886, SD 210/SD 212/SD 205, SD 410/12, SD 425, SD 427, SD 430, SD 435, SD 450, SD 600, SD 615/16/SD 415, SD 625, SD 650/52, SD 810, SD 820, SD 820A, SD 835, SD 845, SD 850, SDA660, SDM429, SDM439, SDM630, SDM632, SDM636, SDM660, SDM710, SDX20, and Snapdragon\_High\_Med\_2016 | [link](https://www.qualcomm.com/company/product-security/bulletins/archives/august-2018#_CVE-2018-5383) |
| Broadcom | BCM4339, BCM4358, and probably many more... | No official publication. |
