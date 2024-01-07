Role Name
=========

Configures a host for SOPS with AGE

Requirements
------------

AGE should already be installed before this role can be used.
That can be done by arikkert.age_binaries.

Role Variables
--------------

parameter variable

    user: this a user that will be configured for this role, so SOPS with AGE. The keys are part of this config

group_vars or host_vars:

    age_public_key: public key for AGE
    age_private_key: private (secret) key for AGE

On https://devops.datenkollektiv.de/using-sops-with-age-and-git-like-a-pro.html is explained how to create the keypair

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: docker
      roles:
         - { role: ansible-role_sops, user: docker }

Example Usage of SOPS executable
--------------------------------

sops README.sops	# creates/edits README.sops and encrypt it with the AGE key

License
-------

BSD

Author Information
------------------

ARK-ICT
