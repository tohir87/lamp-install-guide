# lamp-install-guide
# https://www.digitalocean.com/community/tutorials/how-to-install-lamp-on-ubuntu-14-04-quickstart
LAMP installation on linux
Step 1: Update apt-get package lists
sudo apt-get update
Step 2: Install Apache, MySQL, and PHP packages
sudo apt-get -y install apache2 mysql-server php5-mysql php5 libapache2-mod-php5 php5-mcrypt
Step 3: Create MySQL database directory structure
sudo mysql_install_db
Step 4: Run basic MySQL security script
sudo mysql_secure_installation
Step 5: Configure Apache to prioritize PHP files (optional)
Open Apache's dir.conf file in a text editor:
sudo nano /etc/apache2/mods-enabled/dir.conf
Edit the DirectoryIndex directive by moving index.php to the first item in the list, so it looks like this:
dir.conf — updated DirectoryIndex
DirectoryIndex index.php index.html index.cgi index.pl index.xhtml index.htm

Restart Apache to put the change into place:
sudo service apache2 restart
