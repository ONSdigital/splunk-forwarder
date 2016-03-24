Role Name
=========

This role installs the Splunk forwarder, configures basic log watching and forwards those to Splunk.

Requirements
------------
None


Role Variables
--------------

Variables with defaults:

* `splunk_server`: IP:PORT of the splunk server to forward to.
* `splunk_dir`: Path to the splunk directory, the debian package installs to /opt/splunk/ by default.
* `splunk_download_url`: Full qualified url to a debian install package
* `splunk_download_md5`: md5 checksum of the package to install. Used verify the package from Splunk.

Variables:

* `splunk_log_items`: A set of log files to forward to splunk.
```
- splunk_log_items:
  - app_name: custom
    source: "/var/log/messages"
    index: "syslog"
    sourcetype: linux_messages_syslog
```




Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- hosts: all
  gather_facts: true
  roles:
  - role: splunk-forwarder

License
-------

MIT

Crown Copyright 2016 ONS(UK Office of National Statistics) Digital
Authors: Dan Hilton
------------------


http://blog.ons.digital/
