Role Name
=========

docker

This role installs Docker Engine (CE) on Ubuntu-based systems using the official Docker repository. It also configures Docker to run as a systemd service, adds the current user to the docker group, and ensures connection is re-established after group changes.



Requirements
------------
* Target system must be Ubuntu (tested with 20.04+).

* Python must be installed on the managed host.

* The user running the playbook should have sudo privileges.

* ansible_user should match the SSH login user (used to add to the docker group).

* Ensure internet access is available for downloading Docker packages and the GPG key.

Example Playbook
----------------


    - name: Install and configure Docker
      hosts: aws
      become: true
      roles:
        - docker


