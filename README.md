# ansible-bootstrap-system
Ansible role used to setup a freshly created operating system

## Usage

    - name: Do OS-ready configuration
      hosts: all
      roles:
        - role: bootstrap-system
      vars:
        bootstrap_syslog_target_host: my-syslog.local
        bootstrap_set_hostname_from_inventory: true

        bootstrap_htpdate_servers:
          - http://www.wikipedia.org

        bootstrap_http_proxy_packages_per_repo:
          - host: "archive.ubuntu.com"
            proxy: "http://my-proxy.local:3128"
