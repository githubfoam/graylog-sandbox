# graylog-sandbox
=========
graylog testing


----------------

Playbook
----------------


File:

    - hosts: servers
      roles:
      - elastic-search
      - graylog
      - graylog-client
      - mongodb
      - openjdk
      - https://github.com/githubfoam/ansible-role-apache2.git

Command:

git clone this-project  
vagrant up control-machine  
vagrant up ansi01  
ansi01 - graylog server  
http://192.168.45.21:9000  
login : user/password admin/yourpassword    
control-machine - apache2 server  
http://192.168.45.21  

Graylog Server Configuration Steps:  Add input node
System Menu
Inputs  
Select Input -> Syslog UDP  
Launch New Input  
Node -> ansi01  
Title -> Syslog UDP  
Port -> 5140  
Save  


License
-------

GNU General Public License v3.0

Author Information
------------------

An optional section for the role authors
