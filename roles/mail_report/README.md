Mail Patch Report
=========

This Ansible role is designed to send an email. To use this role, simply specify the email addresses that should receive the email and configure any additional options as needed.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

| Variable name | Description |
| --- | --- |
| `mail_report_send_to` | The email address that the report should be sent to |
| `mail_report_sender` | The email address that the report will be sent from |
| `mail_report_smtp_host` | The hostname of the SMTP server that will be used to send the email |
| `mail_report_smtp_password` | The password for the SMTP server |
| `mail_report_smtp_port` | The port number of the SMTP server |
| `mail_report_smtp_username` | The username for the SMTP server |
| `mail_report_system_name` | The hostname of the system that the report is being generated for |
| `mail_report_template_reboot_step_reboot_required` | A flag indicating whether or not a reboot is required after patching |
| `mail_report_template_reboot_step_reboot_required_stdout` | Output from the `needs-restarting` command, indicating which processes need to be restarted after patching |

Example Playbook
----------------

    - hosts: servers
      connection: local
      gather_facts: false
      roles:
        - { role: jgoos.patch_workflow.mail_report }
