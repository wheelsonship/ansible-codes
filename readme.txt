note: to configure lamp stack and deploy website using ansible

download the workspace directory 

1. ansible-playbook lampstack_1.yml
2. nano index.html
<!DOCTYPE html>
<html>
  <body>
    <h1>Deployed with Ansible</h1>
  </body>
</html>

3. check localhost on browser to see if lampstack is loaded and apache is working fine displaying the content of index.html

4. make sure you have the users.sql file in the workspace directory from were we are firing commands 
ansible-playbook mysqlmodule.yml

5. nano config.php

change the mysql username and password to mahi and 123456 respectively as the database name is demo by default

6. ensure all the six php files are in the workspace directory to be transferred to the client machine. 

ansible-playbook deploywebsite.yml 

7. check the url on browser http://ipaddressofnode/login.php

the website should be working with database connectivity
