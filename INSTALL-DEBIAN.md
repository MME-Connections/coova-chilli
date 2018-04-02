
#Installation of CoovaChilli on Ubuntu/Debian/Raspbian System

###Install first the dependencies

To make sure coova-chilli will run without any problems, we will install the dependencies first. To do so, run the following commands:

`$ sudo apt-get update`

`$ sudo apt-get install -y -f debhelper devscripts libcurl4-gnutls-dev haserl g++ gengetopt bash-completion libtool libltdl-dev libjson-c-dev libssl-dev make cmake autoconf automake build-essential dpkg-dev`

###Download and install the coova-chilli

Clone the project to your directory

`$ git clone https://github.com/coova/coova-chilli.git`

Once cloned, move inside it. 

`$ cd coova-chilli`

Then build the debian package,

`$ sudo dpkg-buildpackage -us -uc`

After building debian package is done, install the generated .deb file:

`$ sudo dpkg -i coova-chilli_<latest_version_here>_<architecture_here>.deb`

###Starting coova-chilli

To start chilli, run the following command

`$ sudo /etc/init.d/chilli start`
