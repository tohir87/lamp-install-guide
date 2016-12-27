# lamp-install-guide
# https://www.digitalocean.com/community/tutorials/how-to-install-lamp-on-ubuntu-14-04-quickstart
LAMP installation on linux <br>
Step 1: Update apt-get package lists<br>
sudo apt-get update<br>
Step 2: Install Apache, MySQL, and PHP packages<br>
sudo apt-get -y install apache2 mysql-server php5-mysql php5 libapache2-mod-php5 php5-mcrypt<br>
Step 3: Create MySQL database directory structure<br>
sudo mysql_install_db<br>
Step 4: Run basic MySQL security script<br>
sudo mysql_secure_installation<br>
Step 5: Configure Apache to prioritize PHP files (optional)<br>
Open Apache's dir.conf file in a text editor:<br>
sudo nano /etc/apache2/mods-enabled/dir.conf<br>
Edit the DirectoryIndex directive by moving index.php to the first item in the list, so it looks like this:<br>
dir.conf — updated DirectoryIndex<br>
DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm<br>

Restart Apache to put the change into place:<br>
sudo service apache2 restart<br>


=====================================================<br>
sudo apt-get update<br>
sudo apt-get install phpmyadmin<br>
