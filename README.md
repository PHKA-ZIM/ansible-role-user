# User setup automation with ansible

## Installation steps

- Go to you ansible project folder
- Add following to your requirements file

```
- src: https://github.com/PHKA-ZIM/ansible-role-user
  name: ansible-role-user
```

- Install to project roles path
```
ansible-galaxy install -r requirements.yml --roles-path ./roles
```

## Use ansible-role-user

- Import role and override role variables, e.g.
```
- name: Setup user
  roles:
    - role: ansible-role-user
      vars:
        user: banana
        generate_ssh_key: false
```

- All available role vars can be found in `defaults`
