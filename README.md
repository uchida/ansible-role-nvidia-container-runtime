uchida.nvidia-container-runtime
===============================

[![Ansible Role](https://img.shields.io/ansible/role/24081.svg?maxAge=2592000)](https://galaxy.ansible.com/uchida/nvidia-container-runtime/)
![Version](https://img.shields.io/github/tag/uchida/ansible-role-nvidia-container-runtime.svg)
[![License](https://img.shields.io/github/license/uchida/ansible-role-nvidia-container-runtime.svg?maxAge=2592000)](https://tldrlegal.com/license/creative-commons-cc0-1.0-universal)
[![Travis](https://img.shields.io/travis/uchida/ansible-role-nvidia-container-runtime.svg)](https://travis-ci.org/uchida/ansible-role-nvidia-container-runtime)

ansible role to install nvidia-container-runtime and graphics driver

Role Variables
--------------

```
nvidia_container_runtime_version: '*'
nvidia_container_runtime_docker_version: '*'
```

- `nvidia_container_runtime_version` is a variable to specify which version of nvidia-container-runtime, current default value is `'*'`
- `nvidia_container_runtume_docker_version` is a variable to specify which version of docker, current default value is `'*'`

Dependencies
------------

- [uchida.docker](https://galaxy.ansible.com/uchida/docker/): to install docker community edition
- [uchida.nvidia-driver](https://galaxy.ansible.com/uchida/nvidia-driver/): to install NVIDIA Graphics driver
  you may want to select APT repository and driver version, consult README for this role

Example Playbook
----------------

install nvidia-container-runtime:

```
- hosts: servers
  roles:
    - role: uchida.nvidia-container-runtime
```

install nvidia-container-runtime version 1.1.1:

```
- hosts: servers
  roles:
    - role: uchida.nvidia-container-runtime
      nvidia_container_runtime_version: 1.1.1
```

License
-------

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed)

dedicated to public domain, no rights reserved.
