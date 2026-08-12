# Changes to DEB12CIS

## Based on CIS v1.1.0 - Branch align_1.1.0

- align_1.1.0 branch
  - ansible_facts bracket notation applied
  - Audit constants moved to vars/audit.yml
  - audit_bin_validate_certs added and wired to goss download
  - goss updated to v0.5.0, links moved to krameff
  - ansible_vars_goss.yml.j2 renamed lockdown_audit.yml.j2
  - deb12cis_shell_executable added, pipefail applied
  - 3.1.2: orphan warn_control_id removed
  - 1.1.1.9: foreign var prefix corrected
  - 5.2.4: vagrant added to deb12cis_sudoers_exclude_nopasswd_list
  - 5.4.2.7: create_home false added, fixes idempotency for accounts with tmpfs homes
  - benchmark facts gate now tests post_audit_results, post_audit_summary was never defined
  - /tmp handlers made mutually exclusive on deb12cis_tmp_svc
  - tmp.mount.j2: managed-by-Ansible warning typo corrected
  - 1.1.2.x: aligned mount logic and naming
    - redundant prelim_mount_names gate removed from 1.1.2.2.1 - 1.1.2.7.1
    - 1.1.2.1.1 absent/present condition aligned with siblings
    - 1.1.2.3.1 - 1.1.2.7.1 audit sub-task names corrected to benchmark wording
    - 1.1.2.3.1 - 1.1.2.7.1 retagged level2, matching benchmark and audit repo
    - /tmp systemd branch kept as a full tmp.mount unit
  - Update_Initramfs handler added, prelim UAS removal notified a handler that did not exist
  - 6.2.3.6: stray notify to undefined handler 'update auditd' removed
  - 6.1.1.3: journald.conf.d mode converted from octal to symbolic
  - actions/checkout pinned to v7.0.0
  - 5.4.1.x fix file path fro debian pam unix
  - 5.4.1.5: user list detection now compares against deb12cis_inactivelock_lock_days
    - was a fixed 30 day regex, so the 45 day default was re-applied every run
    - stale 30 days or less wording removed from the sub-task name
  - 6.2.4.1: mode corrected to u-x,g-wx,o-rwx, o-x was a typo for u-x
  - 6.2.4.1 - 6.2.4.3: log file group now deb12cis_auditd_log_group, default adm
    - auditd re-applies log_group on every restart, forcing root looped forever
  - auditd template: 99_auditd.rules mode tightened to u-x,g-wx,o-rwx
    - go-wx left the rules world readable until the next run
  - readme updated
  - 7.2.8 updated to exclude non-interactive users
  - many prelim takss moved closer to required tasks

## Based on CIS v1.1.0 - Branch 2026_May_QA

- Update min_ansible_version to 2.16.1
- Remove incorrect 'stig' galaxy tag
- Fix LICENSE company name casing (MindPoint)
- Standardize changelog filename to CHANGELOG.md
- Remove export_badges_public.yml and update_galaxy.yml from private repo
- Add community.docker.docker to container detection
- Rewrite is_container.yml with correct Deb12 CIS rule IDs
- Remove unused deb12cis_selinux_disable variable (addresses DEBIAN12-CIS #141)
- Add container guards to auditd handlers
- Add sshd -t validation to Restart sshd handler
- Fix double-space in handler name (Set reboot required)
- Add args: executable: /bin/bash to piped shell commands (Debian uses dash)
- Fix register order (register after changed_when/failed_when)
- Add no_log to shadow file tasks
- Add file_managed_by_ansible header to audit template
- Fix SELinux references to AppArmor
- Fix sudoers use_pty backrefs silent skip on fresh systems
- Fix goss template 6.1.2.x variables sourcing from wrong rule toggles
- Fix missing opening quote on 3.3.4 task name
- Add no_log to shadow file read task in main.yml
- Convert sshd handler from block to listen pattern (Ansible 2.19 compatibility)
- Add ufw to molecule prepare packages
- Update meta author to Ansible-Lockdown Team
- Create molecule scenarios (default, localhost, wsl) with audit enabled
- Fix check_prereqs.yml: replace libselinux with python3-apt

### March 2026

- renamed several variables inline with remediation role
- deb12cis_gui to deb12cis_desktop_required
- deb12_time_pool_name to deb12_time_pool
- aligned var names with audit to match remediate
- removed unnecessary file and variables
- tidy up
- meta alignment
- title alignment with documentation
- linting and standards

Feb 2026 QA Updates

  - QA updates and linting fixes
    - Updated .ansible-lint config (removed deprecated `parseable` and `verbosity` options)
    - Updated .yamllint config (`comments-indentation` set to `false` for ansible-lint compatibility)
    - Fixed grammar issues across multiple files
      - defaults/main.yml: `wont` -> `won't`, `of of` -> `of`, `variables is` -> `variable is`, `values is` -> `value is`, `5Allow` -> `Allow`, `the the` -> `to the`
      - templates/ansible_vars_goss.yml.j2: `of of` -> `of`
    - Fixed audit template indentation for time_servers block consistency (templates/ansible_vars_goss.yml.j2)
- Added corresponding task to 6.1.3.x `deb12cis_rule_6_1_3_8`
- pre-commit updates
- 4.2.5 variable updates for ports and ntp added logic improved thanks to @Aryvr
- 6.3.2 aide timer added and cron template updates

Aug 2025 Updates

- ansible audit template update for better var usage and aligned with audit
- 1.3.1.4 updated to make ansible-core 2.19 compliant
- 5.3.1.x updated logic improved and ansible-core 2.19 compliant
- thanks to @polski-g
  - issue 85 from public
- thanks to dderemiah
  - issue 98
    - dconf handler name update
    - typo in mode 1.7.2
  - issue 99
    - rsync service name
    - handler systemd_daemon_reload rename
- thanks to @matt-j-griffin
  - auditd template updated for ansible-core 2.19

Oct 2025

- added fixes thanks to @tomtrix and @dvic #96
- added fix for #101 thanks to @aveset
- audit files updated and max-concurrent option added
- workflow updates
- README update
- updated 1.1.1.7 thanks to @aderumier
- audit rules logic updated

July 2025 QA Updates

  - Fix for #89 and #90, thank you @Arvyr

June 2025 QA Updates

  - Update to audit_only to allow fetching results
  - resolved false warning for fetch audit
  - Improved documentation and variable compilation for crypto policies

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
- Rules updated, removed, moved(renumbered), updated
- new functions added
- ansible.facts created
- ability to fetch/copy audit logs to centralised location
- Alignment with 1.0.1 in public

Initial release of playbook
