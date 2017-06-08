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
default_download_path: /tmp
jira_tarball_url: https://www.atlassian.com/software/jira/downloads/binary/atlassian-jira-software-7.3.7.tar.gz
jira_tarball_file: atlassian-jira-software-7.3.7.tar.gz
jira_tarball_directory: atlassian-jira-software-7.3.7-standalone
atlassian_user_name: atlassian
jira_directory: jira
jira_home_directory: jira-home


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
