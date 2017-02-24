# officeonline-install.sh
Script to install Office Online on Ubuntu 16.04 and Debian 8.7 


Written by: Subhi H.<br>
This script is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This script is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/.

It will install libreoffice in/opt/libreoffice, Poco in /opt/poco and onlineOffice in /opt/online

Your can manage your service (systemctl start loolwsd.service) [stop and restart]
Enjoy!!!

INSTALLATION

1. Clone/Download the files:
git clone https://github.com/methuselah-0/officeonlin-install.sh
2. Edit "mydomain" to where you have an existing letsencrypt certificate for.
chmod +x officeonlin-install.sh/officeonline-install.sh
4. Save changes with
Ctrl+x s y and exit with Ctrl+x Ctrl+c
5. Make it executable:
chmod +x officeonlin-install.sh/officeonline-install.sh
5. Run the script
./chmod +x officeonlin-install.sh/officeonline-install.sh

Until prerequisite packages have finished installing you need to be attentive and answer yes to possible questions. After that the building process will run on it's own.

THE INSTALLATION WILL TAKE REALLY VERY LONG TIME SO BE PATIENT PLEASE!!! You may eventually see errors during the installation, just ignore them."
