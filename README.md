Atlassian Jira
=========

Ansible role for installing Atlassian Jira. Tested platforms are:
* Debian 8

Requirements
------------

Debian 8 (jessie)

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

| Parameter | Required | Default | Choices |
| ------------- | ------------- | ------------- | ------------- |
| default_download_path  | yes  | /tmp |  |
| jira_tarball_url  | yes  | https://www.atlassian.com/software/jira/downloads/binary/atlassian-jira-software-7.3.7.tar.gz |  |


Dependencies
------------

    dependencies:
     - role: antonchernik.oracle-jdk

Example 
----------------
    ---
    - hosts: all
      roles:
         - { role: antonchernik.atlassian-jira }

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2017 by [Anton Chernik](https://github.com/antonchernik).
