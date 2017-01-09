# provisioning ssh role

Role to generate ssh key pair and write ~/.ssh/config using a host list defined as follows:

```
ssh_host_list:
  - description: HOME
    hosts:
      - shortname: <server-alias>
        name: <server-full-url>
        user: <server-user>
  - description: WORK
    hosts:
      - shortname: <server-alias>
        ip: <server-ip>
        user: <server-user>
        key: <path-to-ssh-keyfile>
        options:
          - key: ProxyCommand
            value: <proxy-command>
```