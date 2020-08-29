# macOS New User Ansible role

This ansible role implements a subset of commands to `enable` (only) FileVault2 via `fdesetup` present on macOS v10.7 or newer systems.

## Example Playbook

```
    - vars:
        filevault_additional_users_and_passwords:
        - { username: "testuser", password: "test_password" }
        filevault_certificate: yes
        filevault_certificate_file: "/path/to/my/DER.cer"
        filevault_showrecoverykey: yes
    - hosts: localhost
      roles:
      - marcomc.filevault2
```

## Variables

```
verbose:                                  no

```

License
-------

MIT

Author : Marco Massari Calderone (c) 2020 - marco@marcomc.com
