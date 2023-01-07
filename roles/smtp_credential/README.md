Role Name
=========

This Ansible role generates a SMTP credential type in an automation platform. This credential type can be used to store SMTP server login information, such as the hostname, port, and login credentials.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

| Variable name | Description |
| --- | --- |
| `smtp_credential_validate_certs` | A flag indicating whether or not to validate SSL/TLS certificates when connecting to the Automation Controller when creating the credential type |
| `smtp_credential_description` | A description for the SMTP credential |
| `smtp_credential_name` | The name for the SMTP credential |

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

    - hosts: localhost
      connection: local
      become: false
      gather_facts: false
      roles:
         - { role: jgoos.patch_workflow.smtp_credential }
