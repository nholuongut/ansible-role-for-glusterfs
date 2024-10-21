# Ansible Role: GlusterFS

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

Installs and configures GlusterFS on Linux.

## Requirements

For GlusterFS to connect between servers, TCP ports `24007`, `24008`, and `24009`/`49152`+ (that port, plus an additional incremented port for each additional server in the cluster; the latter if GlusterFS is version 3.4+), and TCP/UDP port `111` must be open.

This role performs basic installation and setup of Gluster, but it does not configure or mount bricks (volumes), since that step is easier to do in a series of plays in your own playbook. Ansible 1.9+ includes the [`gluster_volume`](https://docs.ansible.com/ansible/latest/collections/gluster/gluster/gluster_volume_module.html#ansible-collections-gluster-gluster-gluster-volume-module) module to ease the management of Gluster volumes.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    glusterfs_default_release: ""

You can specify a `default_release` for apt on Debian/Ubuntu by overriding this variable. This is helpful if you need a different package or version for the main GlusterFS packages (e.g. GlusterFS 3.5.x instead of 3.2.x with the `wheezy-backports` default release on Debian Wheezy).

    glusterfs_ppa_use: true
    glusterfs_ppa_version: "LATEST"

For Ubuntu, specify whether to use the official Gluster PPA, and which version of the PPA to use. See Gluster's [Getting Started Guide](https://docs.gluster.org/en/latest/Install-Guide/Install/) for more info.

    glusterfs_gpg_key_version: "7"
    glusterfs_deb_version: "LATEST"

For Debian, specify the version of the GPG key and apt package repository to use. See Gluster's [Getting Started Guide](https://docs.gluster.org/en/latest/Install-Guide/Install/) for more info.

## Dependencies

None.

## Example Playbook

    - hosts: server
      roles:
        - nholuong.glusterfs

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
