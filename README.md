Role Name
=========

Creating virtual machines from xml files with libvirt.\n
Have a bootstrap xml config to start vm instantly.\n
In bootstrap config RAM, CPU, Disk can be changed as well\n

Requirements
------------

CPU with virtualization capabilities

Role Variables
--------------

state: may be installed or uninstalled (values: 'install' or 'uninstall')\n
storage_path: path where disk images will be created\n
iso_path: path where downloaded isos will be stored\n

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
