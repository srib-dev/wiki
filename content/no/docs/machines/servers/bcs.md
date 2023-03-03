---
title: "Dell PowerEdge R240 - BCS"
linkTitle: "BCS"
date: 2023-02-05
weight: 2
description: >
  En beskrivelse av maskintjeneren som verter BCS.
---

## Kort forklaring

Denne maskinen er én av 2 maskiner dedikert til tjenester som er nødvendige for at radioen skal kunne ha teknologisk selvstendighet, skulle noe skje med friByte.

Denne maskinen har som hovedoppgave å sørge for at BCS kjører og at MySQL-backupen kjører.

Den er installert med VMWare ESXi 7 Kernel, som kjører virtuelle maskiner. 

## Tjenester

Maskinen er installert med en versjon av VMWare ESXi for å kjøre virtuelle maskiner. På den måten kan vi isolere miljøene for hvert nødvendige program for å forhindre miljøkonflikter mellom programmer. 

Her er en liste over VM-ene som kjører på denne maskinen:

| Navn | Funksjon | OS |
| ---- | -------- | -- |
| BCS og BUS | Kjører BroadCast Server og Broadcast Utility Server | Windows Server 2016 R2|
| MySQL MASTER | Kjører en mysql-klone av DigaSystem-databasen som driftes av friByte | Ubuntu 20.04 |

## Spesifikasjoner

| Feature | Value |
| ------- | ----- |
| Processor | 1x ntel® Xeon® E-2200 product family, Intel Pentium®, Intel Core i3®, Intel Celeron® |
| Memory | 4 x DDR4 DIMM slots, Supports UDIMM, up to 2666MT/s, 64GB Max |

#### Storage controllers

| Feature | Value |
| ------- | ----- |
| Internal controllers | PERC H730P, H330, HBA330 |
| Software RAID | PERC S140 |
| External controllers | 12Gbps SAS HBA |
| Boot Optimized Storage Subsystem (BOSS) | 2 x M.2 240GB (RAID 1 or No RAID) or 1 x M.2 240GB (No RAID only) | 
| Internal Dual SD Module | 2x microSD (16GB, 32GB or 64GB) or 1x microSD (16GB, 32GB or 64GB) |

| | |
| ------- | ----- |
| Drive Bays | Up to 4 x 3.5 cabled SATA, SAS (optional) or SSD*, Up to 4 x 3.5 or 2.5 hot-plug SATA, SAS (optional) or SSD* |
| Power supplies | Single 250W (Bronze) or 450W (Platinum) power supply |

*_available in the hot-plug configuration_

#### Management

| | |
| ------- | ----- |
| Embedded management | iDRAC9, iDRAC Direct |
| OpenManage™ Software | OpenManage Enterprise, OpenManage Power Manager, OpenManage Mobile |

#### I/O & Ports

| | |
| ------- | ----- |
| Networking Options | 2 x 1GbE LOM Network Interface Controller (NIC) ports, 1x USB 2.0, 1 x IDRAC micro USB 2.0 management port, 2 x USB 3.0, VGA, serial connector |
| PCIe | One x8 PCIe Gen 3.0 slot low-profile, half-length with x4 slot width & One x16 PCIe Gen 3.0 slot low-profile/full-height, half-length with x8 bandwith |

#### Connections & Integrations

Connections:

- Nagios Core & Nagios XI
- Micro Focus Operations Manager i (OMi)
- IBM Tivoli Netcool/OMNIbus

Integrations:

- Microsoft® System Center
- VMware® vCenter™
- BMC Truesight (available from BMC)
- Red Hat Ansible

#### Security

- TPM 1.2/2.0 optional
- Cryptographically signed firmware
- Silicon Root of Trust
- Secure Boot
- System Lockdown (requires iDRAC Enterprise or Datacenter)
- System Erase

#### Tools

- iDRAC Service Module
- iDRAC RESTful API with Redfish
- OpenManage Server Administrator
- Dell EMC Repository Manager
- Dell EMC System Update
- Dell EMC Server Update Utility
- Dell EMC Update Catalogs
- Dell EMC RACADM CLI
- IPMI Tool

#### OS Support

- Citrix® XenServer®
- Microsoft® Windows Server® with Hyper-V (2016 and 2019)
- Red Hat® Enterprise Linux
- Ubuntu® Server LTS
- SUSE® Linux Enterprise Server
- VMware® ESXi

#### Dimensions

| | |
| ------- | ----- |
| Form Factor | Rack (1U) |
| Chassis width | 434.00mm (17.08 in) |
| Chassis depth | 573.596mm (22.58 in) (3.5” HDD config) |
| Chassis weight | 12.2 kg (26.89 lb.) |

NB: _These dimensions do not include: bezel, redundant PSU_

### Kilder

[DELL/EMC R240 spec sheet](https://i.dell.com/sites/csdocuments/Product_Docs/en/poweredge-r240-spec-sheet.pdf), sist lest 05.02.23