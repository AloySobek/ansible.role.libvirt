Role Name
=========

Creating virtual machines from xml files with libvirt.
Have a bootstrap xml config to start vm instantly.
In bootstrap config RAM, CPU, Disk can be changed as well

Requirements
------------

CPU with virtualization capabilities

Role Variables
--------------

state: may be installed or uninstalled (values: 'install' or 'uninstall')
storage_path: path where disk images will be created
iso_path: path where downloaded isos will be stored

Dependencies
------------

No dependencies

Example Playbook
----------------

    - hosts: servers
      roles:
         - ansible.role.libvirt
      vars:
        state: 'install'
        storage_path: "/kvm/disks"
        iso_path: "/kvm/iso"

License
-------

MIT

Author Information
------------------

AloySobek
