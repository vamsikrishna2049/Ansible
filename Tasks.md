**Write a task to create the directory ‘/tmp/new_directory’**
- name: Create a new directory
  file:
    path: "/tmp/new_directory"
    state: directory

**Write a task to update and upgrade apt packages**
- name: "update and upgrade apt packages."
  become: yes
  apt:
    upgrade: yes
    update_cache: yes

**PlayBooks**
**Write a playbook that will: a. Install the package zlib b. Create the file /tmp/some_file**

**vi first_playbook.yml**

```
- name: Install zlib and create a file
  hosts: some_remote_host
  tasks:
    - name: Install zlib
      package:
        name: zlib
        state: present
      become: yes
    - name: Create the file /tmp/some_file
      file:
        path: '/tmp/some_file'
        state: touch
```

**Run the playbook on a remote host**
First, edit the inventory file: `vi /etc/ansible/hosts`

```
[some_remote_host]
some.remoted.host.com
```

Run the playbook

`ansible-playbook first_playbook.yml`
