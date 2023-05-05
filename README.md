[![CI](https://github.com/de-it-krachten/ansible-role-common/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-common/actions?query=workflow%3ACI)


# ansible-role-common

Collection of smaller generic tasklist


## Dependencies

#### Roles
None

#### Collections
- community.general

## Platforms

Supported platforms

- Red Hat Enterprise Linux 7<sup>1</sup>
- Red Hat Enterprise Linux 8<sup>1</sup>
- Red Hat Enterprise Linux 9<sup>1</sup>
- CentOS 7
- RockyLinux 8
- RockyLinux 9
- OracleLinux 8
- OracleLinux 9
- AlmaLinux 8
- AlmaLinux 9
- Debian 10 (Buster)
- Debian 11 (Bullseye)
- Ubuntu 18.04 LTS
- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Fedora 36
- Fedora 37

Note:
<sup>1</sup> : no automated testing is performed on these platforms

## Role Variables
### defaults/main.yml
<pre><code>
# default facts to distribute
custom_facts:
  - users
  - groups

# customer facts to distribute
custom_facts_additional: []

# Run setup when facts change
custom_facts_setup: true
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'common'
  hosts: all
  become: "yes"
  tasks:
    - name: Include role 'common'
      ansible.builtin.include_role:
        name: common
</pre></code>
