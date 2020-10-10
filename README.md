[![Build Status](https://travis-ci.org/marcomc/ansible-role-sophos-endpoint.svg?branch=master)](https://travis-ci.org/marcomc/ansible-role-sophos-endpoint)

# sophos-endpoint

Ansible role to configure defaults on OSX.

## Requirements

Ansible 2.0

## Role Variables
```
sophos_app_name: "Sophos Endpoint"  # /Applications/Sophos Endpoint.app
sophos_installer_url: "" # this can be a file:// or http(s):// url
sophos_installer_dir_path: "./sophos_endpoint"
sophos_installer_file_name: "SophosInstaller.zip"
sophos_installer_path: "{{sophos_installer_dir_path}}/{{sophos_installer_file_name}}"
sophos_installer_components_dir: "Sophos Installer Components"
sophos_cloud_config: "{{sophos_installer_dir_path}}/{{sophos_installer_components_dir}}/SophosCloudConfig.plist"
```

## Dependencies

## Example Playbook

```
    - hosts: macos_clients
      vars:
        sophos_installer_url: https://drive.google.com/file/d/xxxyyyzzz

      roles:
         - role: marcomc.macos_sophos_endpoint
```

## License

BSD

## Author Information
