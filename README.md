# Ansible Collection - jgoos.patching

Ansible Collection for patching RHEL systems via a workflow in Ansible Automation Platform.  
This workflow is designed to allow system owners to easily patch their systems through the automation platform.


# Patching Workflow in the ansible Automation Platform

## Workflow Steps

1.  **Input:** The system owner provides the necessary input, such as the list of systems to be patched. The system owner can also indicate whether a reboot is desired.
2.  **Sanitize input:** The input is sanitized to ensure that it is in the correct format and does not contain any malicious content.
3.  **Pre-patch checks:** The automation platform performs a series of pre-patch checks to ensure that the systems are ready to be patched and that there will be no negative impacts on the systems as a result of the patching process.
4.  **Reboot:** If necessary, the systems are rebooted to apply the patches. If the system owner indicated that a reboot is desired, this step will be performed.
5.  **Post-patch checks:** The automation platform performs a series of post-patch checks to ensure that the patches were applied correctly and that the systems are functioning properly.
6.  **Email system owner:** The system owner is notified via email that the patching process has been completed. If a reboot was not requested, the email will include a note that a reboot may still be necessary in order for the patches to take effect.

## Playbooks

- jgoos.patching.patch_system.yml
- jgoos.patching.post_patching_checks.yml
- jgoos.patching.pre_patching_checks.yml
- jgoos.patching.reboot_system.yml
- jgoos.patching.sanitize_input.yml
- jgoos.patching.send_email.yml
