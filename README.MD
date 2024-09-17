jenkinsfile run its ask copy permission cp -r 

sudo visudo
##Add a rule to allow the Jenkins user to execute the necessary commands without a password.

jenkins ALL=(ALL) NOPASSWD: /bin/mkdir, /bin/cp


##Ensure Jenkins has the required permissions: You can configure the /var/www/dog directory and other required directories to be accessible by the Jenkins user

sudo chown -R jenkins:jenkins /var/www/dog



jenkins ALL=(ALL) NOPASSWD: /usr/bin/cp

sudo chown -R jenkins:jenkins /var/www/dog

sudo chmod -R 755 /var/www/dog



