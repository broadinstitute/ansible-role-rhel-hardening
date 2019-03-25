# ansible-role-rhel-hardening

### Overview:
- A collection of NIST ansible playbok to meet specific security requirements.

### Usage:
- A playbook is selected by setting the policy variable

```
---
policy: 800-171

```
#### Possible selections are the following
- #### stig-rhel7-disa
  - This profile contains configuration checks that align to the DISA STIG for Red Hat Enterprise Linux V1R4.
    - **Not applicable to CentOS Linux, included for reference only**
- #### standard
  - This profile contains rules to ensure standard security baseline of a Red Hat Enterprise Linux 7 system. Regardless of your system's workload all of these checks should pass.
- #### rht-ccp
  - This profile contains the minimum security relevant configuration settings recommended by Red Hat, Inc for Red Hat Enterprise Linux 7 instances deployed by Red Hat Certified Cloud Providers.
- #### pci-dss
  - Ensures PCI-DSS v3 related security configuration settings are applied.
- #### ospp42
  - This profile reflects mandatory configuration controls identified in the NIAP Configuration Annex to the Protection Profile for General Purpose Operating Systems (Protection Profile Version 4.2).
- #### ospp
  -  This baseline implements configuration requirements from the following
    - sources:
      - Committee on National Security Systems Instruction No. 1253 (CNSSI 1253)
      - NIST Controlled Unclassified Information (NIST 800-171)
      - NIST 800-53 control selections for MODERATE impact systems (NIST 800-53)
      - U.S. Government Configuration Baseline (USGCB)
      - NIAP Protection Profile for General Purpose Operating Systems v4.0 (OSPP v4.0)
      - DISA Operating System Security Requirements Guide (OS SRG)

- #### nist-800-171
  - This profile configures Red Hat Enterprise Linux 7 to the NIST Special Publication 800-53 controls identified for securing Controlled Unclassified Information (CUI).
- #### hipaa
  - This profile configures Red Hat Enterprise Linux 7 to the HIPAA Security Rule identified for securing of electronic protected health information.
- #### cjis
  - This profile is derived from FBI's CJIS v5.4 Security Policy. A copy of this policy can be found at the CJIS Security
- #### c2s
  - This profile demonstrates compliance against the
   U.S. Government Commercial Cloud Services (C2S) baseline.
   This baseline was inspired by the Center for Internet Security (CIS) Red Hat Enterprise Linux 7 Benchmark, v2.1.1 - 01-31-2017.


   #### Sample playbook
   ```
---
- hosts: localhost
  tasks:
  - include_role:
      name: ansible-role-rhel-hardening
    ignore_errors: yes

  ```
