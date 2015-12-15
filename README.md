Ansible role for install and configure virtualenvwrapper
========================================

Configuration by [https://virtualenvwrapper.readthedocs.org/en/latest/](https://virtualenvwrapper.readthedocs.org/en/latest/)

Installation methods
--------------------
* Binary packages from the github repository (role name: ansible.virtualenvwrapper)
* Ansible Galaxy: ansible-galaxy install lciolecki.virtualenvwrapper (role name: lciolecki.virtualenvwrapper) 
 
Recommended way installation is ansible galaxy.

Usage
-----

```yaml
---
- hosts: all

  roles:
    - lciolecki.virtualenvwrapper

  vars:
  ....
```

Variables
---------

```yaml
---
virtualenvwrapper_version: 4.7

virtualenvwrapper_python: /usr/bin/python

virtualenvwrapper_virtualenv: /usr/local/bin/virtualenv

virtualenvwrapper_source: /usr/local/bin/virtualenvwrapper.sh

virtualenvwrapper_home: "{{ lookup('env', 'HOME') }}/.virtualenvs/"

virtualenvwrapper_project: "{{ lookup('env', 'HOME') }}/projects/"

virtualenvwrapper_shell_file: "{{ lookup('env', 'HOME') }}/.bashrc"

```

License
-------
The MIT License (MIT)

Copyright (c) 2015 Łukasz Ciołecki

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.