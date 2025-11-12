# 🜂 Noreum Core Stack Overview

**Build version:** v1.0.0-local  
**Release date:** 2025-11-12  
**Maintainer:** Noreum Core Team <sign@noreum.org>  
**Chain ID:** 1177  
**Network:** Noreum Mainnet (Layer 1)

---

##  Execution Layer (EL)
**Client:** [Noreum Execution Client](https://github.com/noreum/noreum-geth)  
**Base:** go-ethereum v1.16.7 @ b9f3a3d9  
**Binary:** `/usr/local/bin/noreum-geth`  
**SHA256:** `d72a4ed62b3e2ef46400991130e23fd3386ee3ae99fe277ed1be97c539433cd8`  
**License:** Noreum License Override (derived from GPLv3)  
**Notes:** Static bootnodes, no Ethereum discovery, Deneb→Cancun enabled.

---

##  Consensus Layer (CL)
**Client:** [Noreum Beacon Node](https://github.com/noreum/noreum-beacon)  
**Base:** Prysm v6.1.4 @ OffchainLabs  
**Binary:** `/usr/local/bin/noreum-beacon`  
**SHA256:** `41899964ae57e657aae0a2142db98083c23ffdda37b156e9376d8198895191e5`  
**License:** Noreum License Override (derived from Apache-2.0)  
**Notes:** CL/EL handshake verified, isolated from Ethereum endpoints.

---

##  Build Manifest
**File:** `noreum_build_manifest_v1.txt`  
**Location:** `/var/noreum/nucleus/manifests/FINAL/`  
**Manifest SHA256:** `0eebbcd11fa42b58a31266f7be0b71b0d515d653050af35ffa4a6bf714b03ef9`  
**Signature:** GPG Key `1630 2607 60FF 2811 C5BA 73B1 4763 88C3 965F CDFF`  
**Status:** Valid signature (verified)  
**Purpose:** Links EL + CL binaries to chain ID 1177 with auditable checksum record.

---

##  Integrity Verification
Run on any node:
 Repository Map
Component	Repository	License	Release
Execution Client	noreum-geth
	Noreum Override (GPLv3 base)	v1.0.0-local
Consensus Client	noreum-beacon
	Noreum Override (Apache base)	v1.0.0-local
Build Manifest	manifest-signing
	—	v1.0.0

End of Document — Noreum Core Stack 2025

sha256sum noreum-geth noreum-beacon
gpg --verify noreum_build_manifest_v1.txt.asc noreum_build_manifest_v1.txt
