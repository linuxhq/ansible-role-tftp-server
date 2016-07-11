# ansible-role-tftp-server

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-tftp-server.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-tftp-server)

RHEL/CentOS - Trivial File Transfer Protocol

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    tftp_server_cps: [ '100', '2' ]
    tftp_server_disable: True
    tftp_server_flags: IPv4
    tftp_server_per_source: 11
    tftp_server_protocol: udp
    tftp_server_socket_type: dgram
    tftp_server_server: /usr/sbin/in.tftpd
    tftp_server_server_args: '-s /var/lib/tftpboot'
    tftp_server_user: root
    tftp_server_wait: True

The tftp-server service is disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.tftp-server
          tftp_server_disable: False

## License

BSD

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
