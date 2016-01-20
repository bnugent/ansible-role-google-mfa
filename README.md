Role Name
=========

This role installs and configures the Google 2-factor Auth PAM module for linux.

Role Variables
--------------

* `google_mfa_pkg_name` - Name of the Google Auth Pam package
* `google_mfa_pkg_state` - Google Auth Pam package state
* `google_mfa_config_usergroup` - Group name for users you want to use Google Auth
* `google_mfa_users` - List of usernames to enroll
* `google_mfa_enroll_users` - Whether to enroll users (default) or just set up mfa
* `google_mfa_openssh_service_name` - OpenSSH service name


Dependencies
------------

none

Example Playbook
----------------

    - hosts: servers
      vars:
        google_mfa_users:
          - foo
          - bar
      roles:
         - google_mfa

License
-------

MIT

Author Information
------------------

Role created by Ben Nugent.
