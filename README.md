# ansible-role-tftp_server

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-tftp_server.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-tftp_server)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-tftp_server-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/tftp_server)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

RHEL/CentOS - Trivial File Transfer Protocol

## Requirements

This role requires that you have xinetd installed.

 * https://galaxy.ansible.com/linuxhq/xinetd/

## Role Variables

Available variables are listed below, along with default values:

    tftp_server_cps: 100 2
    tftp_server_disable: true
    tftp_server_flags: IPv4
    tftp_server_per_source: 11
    tftp_server_protocol: udp
    tftp_server_socket_type: dgram
    tftp_server_server: /usr/sbin/in.tftpd
    tftp_server_server_args: '-s /var/lib/tftpboot'
    tftp_server_user: root
    tftp_server_wait: true

The tftp-server service is disabled by default.

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.tftp_server
          tftp_server_disable: false

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
