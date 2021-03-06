Atlassian Jira
=========

Ansible role for installing Atlassian Jira. Tested platforms are:
* Debian 8
* Ubuntu 16


Requirements
------------

Debian 8 (jessie)
Ubuntu 16 (xenial)


Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

| Parameter | Required | Default | Choices | Comments |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| default_download_directory | no | /tmp | | Sets directory where files will be downloaded |
| jira_version  | no | 7.8.2 | | Sets Atlassian Jira version for installing  |
| atlassian_user_name | no  | atlassian | | Sets Jira system user to run with /sbin/nologin |
| jira_port | no | 8080 | | Set jira port
| jira_proxy_host | no | | | Set jira proxy host
| jira_context_path | no | | | Set jira context path. Example http://mydomain.com:8080[:jira_context_path]
| jira_proxy_port | no | | | Set jira proxy port. Should be set for any proxy host
| jira_proxy_https | no | false | | Set if proxy works with https
| jira_directory | no  | jira | | Sets Jira directory name. Example /home/[:atlassian_user_name]/[:jira_directory] |
| jira_home_directory | no  | jira-home | | Sets Jira directory for all file. Example /home/[:atlassian_user_name]/[:jira_home_directory] |
| java_home | no  | /usr/lib/jvm | | Sets path to JAVA_HOME |
| java_mysql_connector_version | no  | 5.1.46 | | Sets version for MySQL java connector |





Dependencies
------------

    dependencies:
     - role: geerlingguy.java

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
