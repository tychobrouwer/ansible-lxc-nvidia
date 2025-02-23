Install and configure nvidia drivers in LXC containers
=========

The role installs and configures nvidia drivers in LXC containers (and the host).

It should be run on the host and the container with the same variables.

<https://theorangeone.net/posts/lxc-nvidia-gpu-passthrough/>

<https://matthieu.yiptong.ca/2020/12/06/nvidia-gpu-passthrough-to-lxc-containers-on-proxmox-6-for-nvenc-in-plex/>

Role Variables
--------------

The ```lxc_nvidia_version``` variable should be set to the full version number of the driver to be installed

```lxc_nvidia_lxc_id``` should be set to the container id of the container to install the drivers in

```lxc_nvidia_is_host``` should be set to true if the role is run on the host, false if it is run in the container

Example Playbook
----------------

```yaml
- hosts: host
  vars:
    lxc_nvidia_is_host: true
    lxc_nvidia_lxc_id: 101
    lxc_nvidia_version: 535.154.05

  roles:
    - role: tychobrouwer.lxc_nvidia

- hosts: lxc
  vars:
    lxc_nvidia_is_host: false
    lxc_nvidia_lxc_id: 101
    lxc_nvidia_version: 535.154.05

  roles:
    - role: tychobrouwer.lxc_nvidia
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
