# Changes to DEB12CIS

## 1.2.0 Based on CIS v1.1.0

July 2025 QA Updates
  - Fix for #89 and #90, thank you @Arvyr

June 2025 QA Updates
  - Update to audit_only to allow fetching results
  - resolved false warning for fetch audit
  - Improved documentation and variable compilation for crypto policies

- ADDED ITEMS:
  1.1.0 ADDED RECOMMENDATION: 1.1.1.6 - Ensure overlayfs kernel module is not available
  1.1.0 ADDED RECOMMENDATION: 1.1.1.10 - Ensure unused filesystems kernel modules are not available
  1.1.0 ADDED RECOMMENDATION: 1.7.10 - Ensure XDMCP is not enabled
  1.1.0 ADDED SECTION: 4.1 - Configure a single firewall utility
  1.1.0 ADDED RECOMMENDATION: 4.1.1 - Ensure a single firewall configuration utility is in use
  1.1.0 ADDED RECOMMENDATION: 4.4.1.2 - Ensure nftables is not in use with iptables
  1.1.0 ADDED RECOMMENDATION: 4.4.1.3 - Ensure ufw is not in use with iptables
  1.1.0 ADDED RECOMMENDATION: 5.4.1.2 - Ensure minimum password days is configured
  1.1.0 ADDED RECOMMENDATION: 5.4.2.4 - Ensure root account access is controlled
  1.1.0 ADDED RECOMMENDATION: 6.1.1.4 - Ensure only one logging system is in use
  1.1.0 ADDED RECOMMENDATION: 6.1.2.1.2 - Ensure systemd-journal-upload authentication is configured
  1.1.0 ADDED SECTION: 6.1.3 - Configure rsyslog
  1.1.0 ADDED RECOMMENDATION: 6.1.3.1 - Ensure rsyslog is installed
  1.1.0 ADDED RECOMMENDATION: 6.1.3.2 - Ensure rsyslog service is enabled and active
  1.1.0 ADDED RECOMMENDATION: 6.1.3.3 - Ensure journald is configured to send logs to rsyslog
  1.1.0 ADDED RECOMMENDATION: 6.1.3.4 - Ensure rsyslog log file creation mode is configured
  1.1.0 ADDED RECOMMENDATION: 6.1.3.5 - Ensure rsyslog logging is configured
  1.1.0 ADDED RECOMMENDATION: 6.1.3.6 - Ensure rsyslog is configured to send logs to a remote log host
  1.1.0 ADDED RECOMMENDATION: 6.1.3.7 - Ensure rsyslog is not configured to receive logs from a remote client
  1.1.0 ADDED RECOMMENDATION: 6.1.3.8 - Ensure logrotate is configured
  1.1.0 ADDED RECOMMENDATION: 6.2.1.1 - Ensure auditd packages are installed
  1.1.0 ADDED RECOMMENDATION: 6.2.3.15 - Ensure successful and unsuccessful attempts to use the chcon command are collected
  1.1.0 ADDED RECOMMENDATION: 6.2.3.16 - Ensure successful and unsuccessful attempts to use the setfacl command are collected
  1.1.0 ADDED RECOMMENDATION: 6.2.3.17 - Ensure successful and unsuccessful attempts to use the chacl command are collected
  1.1.0 ADDED RECOMMENDATION: 6.2.3.18 - Ensure successful and unsuccessful attempts to use the usermod command are collected
  1.1.0 ADDED RECOMMENDATION: 6.2.4.2 - Ensure audit log files owner is configured
  1.1.0 ADDED RECOMMENDATION: 6.2.4.3 - Ensure audit log files group owner is configured
  1.1.0 ADDED RECOMMENDATION: 6.2.4.4 - Ensure the audit log file directory mode is configured
  1.1.0 ADDED RECOMMENDATION: 6.2.4.6 - Ensure audit configuration files owner is configured
  1.1.0 ADDED RECOMMENDATION: 6.2.4.7 - Ensure audit configuration files group owner is configured
  1.1.0 ADDED RECOMMENDATION: 6.2.4.9 - Ensure audit tools owner is configured
  1.1.0 ADDED RECOMMENDATION: 6.2.4.10 - Ensure audit tools
  1.1.0 ADDED RECOMMENDATION: 6.3.3 - Ensure cryptographic mechanisms are used to protect the integrity of audit tools

- DROPPED ITEMS:
  1.1.0 DROPPED RECOMMENDATION: 1.5.4 - Ensure prelink is not installed
  1.1.0 DROPPED RECOMMENDATION: 1.7.10 - Ensure XDCMP is not enabled
  1.1.0 DROPPED RECOMMENDATION: 4.3.1.2 - Ensure nftables is not installed with iptables
  1.1.0 DROPPED RECOMMENDATION: 4.3.1.3 - Ensure ufw is uninstalled or disabled with iptables
  1.1.0 DROPPED RECOMMENDATION: 5.4.1.2 - Ensure minimum password age is configured
  1.1.0 DROPPED RECOMMENDATION: 5.4.2.4 - Ensure root password is set
  1.1.0 DROPPED RECOMMENDATION: 6.2.1.2.2 - Ensure systemd-journal-remote authentication is configured
  1.1.0 DROPPED RECOMMENDATION: 6.3.1.1 - Ensure auditd is installed
  1.1.0 DROPPED RECOMMENDATION: 6.3.3.15 - Ensure successful and unsuccessful attempts to use the chcon command are recorded
  1.1.0 DROPPED RECOMMENDATION: 6.3.3.16 - Ensure successful and unsuccessful attempts to use the setfacl command are recorded
  1.1.0 DROPPED RECOMMENDATION: 6.3.3.17 - Ensure successful and unsuccessful attempts to use the chacl command are recorded
  1.1.0 DROPPED RECOMMENDATION: 6.3.3.18 - Ensure successful and unsuccessful attempts to use the usermod command are recorded
  1.1.0 DROPPED RECOMMENDATION: 6.3.4.2 - Ensure only authorized users own audit log files
  1.1.0 DROPPED RECOMMENDATION: 6.3.4.3 - Ensure only authorized groups are assigned ownership of audit log files
  1.1.0 DROPPED RECOMMENDATION: 6.3.4.4 - Ensure the audit log directory mode is configured
  1.1.0 DROPPED RECOMMENDATION: 6.3.4.6 - Ensure audit configuration files are owned by root
  1.1.0 DROPPED RECOMMENDATION: 6.3.4.7 - Ensure audit configuration files belong to group root
  1.1.0 DROPPED RECOMMENDATION: 6.3.4.9 - Ensure audit tools are owned by root
  1.1.0 DROPPED RECOMMENDATION: 6.3.4.10 - Ensure audit tools belong to group root

- MOVED ITEMS:
  1.1.0 MOVED RECOMMENDATION: 1.1.1.7 - Ensure squashfs kernel module is not available moved from 1.1.1.6 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 1.1.1.8 - Ensure udf kernel module is not available moved from 1.1.1.7 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 1.1.1.9 - Ensure usb-storage kernel module is not available moved from 1.1.1.8 in 1.0.1
  1.1.0 MOVED SECTION: 4.2 - Configure UncomplicatedFirewall moved from 4.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.2.1 - Ensure ufw is installed moved from 4.1.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.2.2 - Ensure iptables-persistent is not installed with ufw moved from 4.1.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.2.3 - Ensure ufw service is enabled moved from 4.1.3 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.2.4 - Ensure ufw loopback traffic is configured moved from 4.1.4 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.2.5 - Ensure ufw outbound connections are configured moved from 4.1.5 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.2.6 - Ensure ufw firewall rules exist for all open ports moved from 4.1.6 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.2.7 - Ensure ufw default deny firewall policy moved from 4.1.7 in 1.0.1
  1.1.0 MOVED SECTION: 4.3 - Configure nftables moved from 4.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.3.1 - Ensure nftables is installed moved from 4.2.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.3.2 - Ensure ufw is uninstalled or disabled with nftables moved from 4.2.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.3.3 - Ensure iptables are flushed with nftables moved from 4.2.3 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.3.4 - Ensure a nftables table exists moved from 4.2.4 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.3.5 - Ensure nftables base chains exist moved from 4.2.5 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.3.6 - Ensure nftables loopback traffic is configured moved from 4.2.6 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.3.7 - Ensure nftables outbound and established connections are configured moved from 4.2.7 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.3.8 - Ensure nftables default deny firewall policy moved from 4.2.8 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.3.9 - Ensure nftables service is enabled moved from 4.2.9 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.3.10 - Ensure nftables rules are permanent moved from 4.2.10 in 1.0.1
  1.1.0 MOVED SECTION: 4.4 - Configure iptables moved from 4.3 in 1.0.1
  1.1.0 MOVED SECTION: 4.4.1 - Configure iptables software moved from 4.3.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.4.1.1 - Ensure iptables packages are installed moved from 4.3.1.1 in 1.0.1
  1.1.0 MOVED SECTION: 4.4.2 - Configure IPv4 iptables moved from 4.3.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.4.2.1 - Ensure iptables default deny firewall policy moved from 4.3.2.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.4.2.2 - Ensure iptables loopback traffic is configured moved from 4.3.2.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.4.2.3 - Ensure iptables outbound and established connections are configured moved from 4.3.2.3 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.4.2.4 - Ensure iptables firewall rules exist for all open ports moved from 4.3.2.4 in 1.0.1
  1.1.0 MOVED SECTION: 4.4.3 - Configure IPv6 ip6tables moved from 4.3.3 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.4.3.1 - Ensure ip6tables default deny firewall policy moved from 4.3.3.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.4.3.2 - Ensure ip6tables loopback traffic is configured moved from 4.3.3.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.4.3.3 - Ensure ip6tables outbound and established connections are configured moved from 4.3.3.3 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 4.4.3.4 - Ensure ip6tables firewall rules exist for all open ports moved from 4.3.3.4 in 1.0.1
  1.1.0 MOVED SECTION: 6.1 - System Logging moved from 6.2 in 1.0.1
  1.1.0 MOVED SECTION: 6.1.1 - Configure systemd-journald service moved from 6.2.1.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.1.1.1 - Ensure journald service is enabled and active moved from 6.2.1.1.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.1.1.2 - Ensure journald log file access is configured moved from 6.2.1.1.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.1.1.3 - Ensure journald log file rotation is configured moved from 6.2.1.1.3 in 1.0.1
  1.1.0 MOVED SECTION: 6.1.2 - Configure journald moved from 6.2.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.1.2.2 - Ensure journald ForwardToSyslog is disabled moved from 6.2.1.1.4 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.1.2.3 - Ensure journald Compress is configured moved from 6.2.1.1.6 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.1.2.4 - Ensure journald Storage is configured moved from 6.2.1.1.5 in 1.0.1
  1.1.0 MOVED SECTION: 6.1.2.1 - Configure systemd-journal-remote moved from 6.2.1.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.1.2.1.1 - Ensure systemd-journal-remote is installed moved from 6.2.1.2.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.1.2.1.3 - Ensure systemd-journal-upload is enabled and active moved from 6.2.1.2.3 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.1.2.1.4 - Ensure systemd-journal-remote service is not in use moved from 6.2.1.2.4 in 1.0.1
  1.1.0 MOVED SECTION: 6.1.4 - Configure Logfiles moved from 6.2.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.1.4.1 - Ensure access to all logfiles has been configured moved from 6.2.2.1 in 1.0.1
  1.1.0 MOVED SECTION: 6.2 - System Auditing moved from 6.3 in 1.0.1
  1.1.0 MOVED SECTION: 6.2.1 - Configure auditd Service moved from 6.3.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.1.2 - Ensure auditd service is enabled and active moved from 6.3.1.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.1.3 - Ensure auditing for processes that start prior to auditd is enabled moved from 6.3.1.3 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.1.4 - Ensure audit_backlog_limit is sufficient moved from 6.3.1.4 in 1.0.1
  1.1.0 MOVED SECTION: 6.2.2 - Configure Data Retention moved from 6.3.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.2.1 - Ensure audit log storage size is configured moved from 6.3.2.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.2.2 - Ensure audit logs are not automatically deleted moved from 6.3.2.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.2.3 - Ensure system is disabled when audit logs are full moved from 6.3.2.3 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.2.4 - Ensure system warns when audit logs are low on space moved from 6.3.2.4 in 1.0.1
  1.1.0 MOVED SECTION: 6.2.3 - Configure auditd Rules moved from 6.3.3 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.1 - Ensure changes to system administration scope (sudoers) is collected moved from 6.3.3.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.2 - Ensure actions as another user are always logged moved from 6.3.3.2 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.3 - Ensure events that modify the sudo log file are collected moved from 6.3.3.3 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.4 - Ensure events that modify date and time information are collected moved from 6.3.3.4 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.5 - Ensure events that modify the system's network environment are collected moved from 6.3.3.5 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.6 - Ensure use of privileged commands are collected moved from 6.3.3.6 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.7 - Ensure unsuccessful file access attempts are collected moved from 6.3.3.7 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.8 - Ensure events that modify user/group information are collected moved from 6.3.3.8 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.9 - Ensure discretionary access control permission modification events are collected moved from 6.3.3.9 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.10 - Ensure successful file system mounts are collected moved from 6.3.3.10 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.11 - Ensure session initiation information is collected moved from 6.3.3.11 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.12 - Ensure login and logout events are collected moved from 6.3.3.12 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.13 - Ensure file deletion events by users are collected moved from 6.3.3.13 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.14 - Ensure events that modify the system's Mandatory Access Controls are collected moved from 6.3.3.14 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.19 - Ensure kernel module loading unloading and modification is collected moved from 6.3.3.19 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.20 - Ensure the audit configuration is immutable moved from 6.3.3.20 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.3.21 - Ensure the running and on disk configuration is the same moved from 6.3.3.21 in 1.0.1
  1.1.0 MOVED SECTION: 6.2.4 - Configure auditd File Access moved from 6.3.4 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.4.1 - Ensure audit log files mode is configured moved from 6.3.4.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.4.5 - Ensure audit configuration files mode is configured moved from 6.3.4.5 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.2.4.8 - Ensure audit tools mode is configured moved from 6.3.4.8 in 1.0.1
  1.1.0 MOVED SECTION: 6.3 - Configure Integrity Checking moved from 6.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.3.1 - Ensure AIDE is installed moved from 6.1.1 in 1.0.1
  1.1.0 MOVED RECOMMENDATION: 6.3.2 - Ensure filesystem integrity is regularly checked moved from 6.1.2 in 1.0.1

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
