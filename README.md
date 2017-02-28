# officeonline-install.sh by husisusi

Script to install Office Online on Ubuntu 16.04 and Debian 8.7 

Written by: Subhi H.<br>
This script is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This script is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/.

## This Fork Info
Reasons:
  - Builds were not working so I tried to make this fork more failsafe by having source versions set to known-to-work commits.
  - I also wanted a more commented version to better understand the installation process.

I used this script with Nextcloud running on Debian Testing with nginx, mariadb, and php7 with the following sources and commit versions:
  - LibreOffice Core commit=4c0040b6f1e3137e0d40aab09088c43214db3165 url=https://github.com/LibreOffice/core.git
  - Poco=poco-1.7.7-all.tar.gz url: http://pocoproject.org/releases/poco-1.7.7/poco-1.7.7-all.tar.gz
  - LibreOffice Online=91666d7cd354ef31344cdd88b57d644820dcd52c url=https://github.com/LibreOffice/online
It will install LibreOffice Core in /opt/core, Poco in /opt/poco and LibreOffice Online in /opt/online and you will get the LibreOffice Online web-socket daemon (loolwsd) running on localhost:9980 which you can connect to from Nextcloud. Your can manage your service with systemctl start/stop/status loolwsd.service.

Enjoy!!!

## Prerequisites
It's intended to be used with a running NextCloud server.

You should have setup valid letsencrypt certificates for your domain in /etc/letsencrypt/<mydomain>.tld/*

## Installation
1. Clone/Download the files:
git clone https://github.com/methuselah-0/officeonlin-install.sh
2. Edit "mydomain" passwords etc. to where you have your existing letsencrypt certificates.
cd libre-office-online && zile install.sh
4. Save changes with
Ctrl+x s y and exit with Ctrl+x Ctrl+c
5. Make it executable:
sudo chmod +x install.sh
5. Run the script
sudo ./install.sh
6. Login as admin in your nextcloud instance and go to apps section and enable the Collabora Online app. Then to Admin->Admin->Collabora Online and enter your url and port number. (e.g. if you visit your cloud instance at https://nextcloud.selfhosted.xyz you would enter https://nextcloud.selfhosted.xyz:9980 )
Read the first run info dialog box and then the building process should run on it's own.

THE INSTALLATION WILL TAKE REALLY VERY LONG TIME SO BE PATIENT PLEASE!!! You may eventually see errors during the installation, just ignore them."
