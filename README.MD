sysctl
========

sysctl - role for configure kernel parameters at runtime and set at boot
(persist parameters).

Requirements for usage
-------------------------

* Ansible 2.2;
* jmespath;

Example configuration
-------------------------

```yaml
---
sysctl:
# This file will be saved on `sysctl.d`.
- file: '99-linux'
  options:
  - name: 'kernel.panic'
    value: '0'
  - name: 'fs.inotify.max_user_watches'
    value: '100000'
```
