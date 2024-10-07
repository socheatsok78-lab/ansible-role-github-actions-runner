# ansible-role-github-actions-runner
Ansible Role - GitHub Actions Runner

## Role Variables
Available variables are listed below, along with default values (see `defaults/main.yml`):

```yml
github_pat: "token"
github_organization: "organization"

github_actions_runner_state: present # or absent (default: present)
```

## Add to `requirements.yml`

```yml
roles:
  - name: socheatsok78-lab.github-actions-runner
    src: https://github.com/socheatsok78-lab/ansible-role-github-actions-runner
    version: main
    scm: git
```

## Use with Ansible

Example:

```yml
- hosts: all
  become: true
  vars:
    github_pat: "your-github-token-here"
    github_organization: "your-github-organization"
  roles:
    - socheatsok78-lab.github-actions-runner
```
