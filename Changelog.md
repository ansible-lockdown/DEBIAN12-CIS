# Changes to DEB12CIS

## 1.1.1 Based on CIS v1.1.0
May 2025
Thank you @DianaMariaDDM
 - Decoupling sshd vars in defaults/main. Adresses #40
Thank you @polski-g for the following:
  - discovered_group_check fix for 7.2.8 based on PR #72
  - failed_when logic improvement based on PR #73
  - /etc/systemd/journald.conf.d improvement on logic for directory existence based on PR #74
  - task/prelim check_mode logic improvement based on PR #75
  - shell logic fix from getent passwd to getent group based on PR #76
- QA Typo Fixes and .github update

Rules updated, removed, moved(renumbered), updated

new functions added
- ansible.facts created
- ability to fetch/copy audit logs to centralised location
Alignment with 1.0.1 in public

## 0.9.0- Based on CIS v1.0.1

- Initial release of playbook
