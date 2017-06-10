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

| Parameter | Required | Default | Choices | Comments |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| default_download_path | yes | /tmp | | Sets directory where files will be downloaded |
| jira_version  | yes | 7.3.7 | | Sets Atlassian Jira version for installing  |
| atlassian_user_name | yes  | atlassian | | Sets Jira system user to run with /sbin/nologin |
| jira_directory | yes  | jira | | Sets Jira directory name. Example /home/[:atlassian_user_name]/[:jira_directory] |
| jira_home_directory | yes  | jira-home | | Sets Jira directory for all file. Example /home/[:atlassian_user_name]/[:jira_home_directory] |
| java_home_directory | yes  | /usr/lib/jvm | | Sets path to JAVA_HOME |
| java_mysql_connector_version | yes  | 5.1.42 | | Sets version for MySQL java connector |





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
