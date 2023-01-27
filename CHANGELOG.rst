===============================
jgoos.patching Release Notes
===============================

.. contents:: Topics

v0.1.0
======

Release Summary
---------------

The first release of the jgoos.patching collection.

New Playbooks
---------

- patch_system.yml
- post_patching_checks.yml
- pre_patching_checks.yml
- reboot_system.yml
- sanitize_input.yml
- send_email.yml

New Roles
---------

- mail_report - Mail patch report to system owner.
- patch - Patch the system.
- post_patch - Perform POST-patch tasks and checks.
- pre_patch - Perform PRE-patch tasks and checks.
- reboot - Reboot the system.
- sanitize_input - Sanitize survey inputs
