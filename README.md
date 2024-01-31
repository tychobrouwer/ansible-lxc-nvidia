Install and configure nvidia drivers in LXC containers
=========

The role installs and configures nvidia drivers in LXC containers (and the host).

<https://theorangeone.net/posts/lxc-nvidia-gpu-passthrough/>

<https://matthieu.yiptong.ca/2020/12/06/nvidia-gpu-passthrough-to-lxc-containers-on-proxmox-6-for-nvenc-in-plex/>

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Example Playbook
----------------

```yaml
    - hosts: servers
      roles:
         - { role: tychobrouwer.lxc_nvidia }
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
