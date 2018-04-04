# ansible-sysctl

sysctl - role for configure kernel parameters at runtime and set at boot
(persist parameters).

## Requirements for usage

* Ansible 2.4;

## Example configuration

```yaml
---
sysctl:
# This file will be saved on `sysctl.d`.
- file: '99-linux'
# Use this option to ignore errors about unknown keys. Default is 'no'.
  ignore_errors: 'no'
  options:
  - name: 'kernel.panic'
    value: '0'
  - name: 'fs.inotify.max_user_watches'
    value: '100000'
```
