Patch System
=========

This ansible role patches Red Hat Enterprise Linux (RHEL) systems. It can be configured to apply security updates, bugfix updates, or both. Additionally, the role checks if a reboot is required after applying patches. To use this role, specify the desired patching configuration and the role will take care of the rest. This role ensures that your RHEL systems are kept up to date and secure.

Role Variables
--------------

| Variable name | Description |
| --- | --- |
| `patch_security_updates` | A flag indicating whether or not to apply security updates |
| `patch_bugfix_updates` | A flag indicating whether or not to apply bugfix updates |
| `patch_check_reboot_needed` | A flag indicating whether or not to check if a reboot is required after applying patches |
| `patch_reboot_required` | A flag indicating whether or not a reboot is required after applying patches |
| `patch_reboot_required_stdout` | Output from the `needs-restarting` command, indicating which processes need to be restarted after patching |

Example Playbook
----------------

    - hosts: servers
      gather_facts: true
      become: true
      roles:
         - { role: jgoos.patch_workflow.patch }
