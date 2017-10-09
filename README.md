Ansible Filebeat for Ubuntu
==

Installs Filebeat on Ubuntu

**Example Play**:
```
---
- hosts: all
  roles:
    - role: ansible-filebeat
      filebeat_logstash_hosts:
        - "my.logstash.server:5044"
      filebeat_pki_keypairs:
        - name: filebeat
          key: "{{ vault_pki_key }}" # contents your key copied into a vault encrypted vars file
          cert: "{{ vault_pki_cert }}" # contents your cert copied into a vault encrypted vars file
```

Requirements
------------
* The target system must have JDK 8 pre-installed.
