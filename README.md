[![Build Status](https://travis-ci.com/marcomc/ansible-role-macos-new-user.svg?branch=master)](https://travis-ci.com/marcomc/ansible-role-macos-new-user)

# macOS New User Ansible role

This ansible role create a new user on the target macOS system.

Used in [Splinter, an opinionated provisioning tool for macOS](https://github.com/marcomc/splinter).

## Example Playbook

    - vars:
        new_user_username:                        "testuser"
        new_user_fullname:                        "Test User"
        new_user_password_cleartext:              "Clear Text Password" # Ansible can only create users on macos using a cleartext password (for now)
    - hosts: localhost
      roles:
      - marcomc.macos_new_user


## Variables

    verbose:                                  no
    new_user_username:                        ""
    new_user_fullname:                        ""
    new_user_shell:                           "/bin/zsh"
    new_user_password_cleartext:              ""
    new_user_generate_ssh_key:                no
    new_user_reset_password_on_login:         yes
    new_user_is_admin:                        yes
    new_user_update_path_for_all_shell_types: no
    new_user_profile_picture_path:            ""
    new_user_random_profile_picture:          no
    new_user_random_profile_pictures_path:    "{{ playbook_dir }}/files/profile_pictures"
    new_user_profile_pictures_filter_formats: 'jpg\|jpeg\|png' # grep filter format


License
-------

[MIT](LICENSE)

Author : Marco Massari Calderone (c) 2020 - marco@marcomc.com
