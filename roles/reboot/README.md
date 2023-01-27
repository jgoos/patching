Reboot systems
=========

This ansible role reboots Red Hat Enterprise Linux (RHEL) systems. A reboot is only performed if two conditions are met: 1) a reboot is selected, and 2) a reboot is required.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

| Variable name | Description |
| --- | --- |
| `reboot_required` | A flag indicating whether or not a reboot is required |
| `reboot_selected` | A flag indicating whether or not a reboot has been selected |

Dependencies
------------

| Variable name | Role | Description |
| --- | --- | --- |
| `patch_reboot_required` | `jgoos.patching.patch` | A flag indicating whether or not a reboot is required after applying patches |
| `patch_reboot_required_stdout` | `jgoos.patching.patch` | Output from the `needs-restarting` command, indicating which processes need to be restarted after patching |
| `sanitize_patch_survey_reboot_requested` | `jgoos.patching.sanitize_input` | A flag indicating whether or not a reboot was requested in the patch survey |


A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

    - hosts: servers
      become: true
      gather_facts: true
      roles:
         - { role: jgoos.patching.reboot }
