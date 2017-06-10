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


    Parameter                    | Required | Default                                      | Choices | Comments
    ---------------------------- | -------- | -------------------------------------------- | ------- | --------
    default_download_path        | yes      | /tmp                                         |         |
    jira_tarball_url             | yes      | https://www.atlassian.com/so...-7.3.7.tar.gz |         |
    jira_tarball_file            | yes      | atlassian-jira-software-7.3.7.tar.gz         |         |
    jira_tarball_directory       | yes      | atlassian-jira-software-7.3.7-standalone     |         |
    atlassian_user_name          | yes      | atlassian                                    |         |
    jira_directory               | yes      | jira                                         |         |
    jira_home_directory          | yes      | jira-home                                    |         |
    java_home_directory          | yes      | /usr/lib/jvm                                 |         |
    java_mysql_connector_version | yes      | 5.1.42                                       |         |


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
