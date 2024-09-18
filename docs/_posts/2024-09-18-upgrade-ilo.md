---
layout: "post"
title: "Upgrade ILO on Gen 8 Microserver (from Fedora Workstation)"
date: "2024-09-18 13:24:10 +0800"
categories: "homelab"
---

1. Go here: https://support.hpe.com/connect/s/softwaredetails?language=en_US&collectionId=MTX-b5848d0ffeab4506&tab=releaseNotes
1. Download the latest Online ROM Flash Component for Linux - HPE Integrated Lights-Out 4 in RPM format
1. Run the following to extract the contents of the RPM: `rpm2cpio firmware-ilo4-2.82-1.1.i386.rpm | cpio -id`
1. Log into ILO web interface
1. Under Administration > Firmware, browse to the following extracted path: `./usr/lib/i386-linux-gnu/firmware-ilo4-2.82-1.1/ilo4_282.bin`
1. Microserver upload firmware and reboot to flash.
