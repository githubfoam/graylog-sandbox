# graylog-sandbox

[![Build Status](https://travis-ci.com/githubfoam/graylog-sandbox.svg?branch=dev)](https://travis-ci.com/githubfoam/graylogy-sandbox)
~~~~
graylog 
https://www.graylog.org  
https://github.com/Graylog2/graylog2-server
elasticsearch  https://www.elastic.co    
mongodb https://www.mongodb.com  
openjdk https://openjdk.java.net      
vagrant https://www.vagrantup.com  
virtualbox https://www.virtualbox.org
~~~~

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

~~~~

git clone this-project  
vagrant up control-machine  (graylof client)
vagrant up ansi01 (ansi01 - graylog server) 

~~~~
~~~~
http://192.168.45.21:9000  
login : user/password admin/yourpassword    

Graylog Dashboard - Web Console
Graylog Server Configuration Steps:  Add input node

Menu Path -  System Menu - Inputs  
Select Input -> Syslog UDP  
Launch New Input  
Node -> ansi01  
Title -> Syslog UDP  
Port -> 5140  
Save  

Menu Path -  System Menu - Nodes

control-machine - apache2 server  
http://192.168.45.20  

~~~~
update graylog
~~~~
roles\graylog\tasks\main.yml

graylog version
https://docs.graylog.org/en/4.1/pages/installation/os/ubuntu.html#ubuntuguide
~~~~
update ubuntu
~~~~

https://githu1b.com/chef/bento/tree/master/packer_templates/ubuntu

~~~~

<div align="center">
    <img src="/screenshots/sysloginput.JPG" width="400px"</img>
</div>



License
-------


GNU General Public License v3.0

Author Information
------------------

An optional section for the role authors
