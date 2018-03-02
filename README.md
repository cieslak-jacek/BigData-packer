Building vmwar images for BigData Cloudera automation 

using Packer builder

Installation of Packer:

1. Download from binary from packer.io
   https://www.packer.io/downloads.html

Packer is packaged as a "zip" file.


Releases page:
   https://releases.hashicorp.com/packer/

File format: (linux) 
   packer_*.*.*_linux_amd64.zip
   ex. packer_1.2.1_linux_amd64.zip


--------------------------------------------
2. Next, unzip the downloaded package into a directory where Packer will be installed. 

  sudo yum install -y unzip
  sudo unzip -d /usr/local packer_0.12.2_linux_amd64.zip

  ~/packer or /usr/local/packer 

is generally good, depending on whether you want to restrict the install 
to just your user or install it system-wide. 


-------------------------------------------
3. Add Packer to enviromental PATH

You need to add it to your ~/.profile or ~/.bashrc file.

  export PATH=$PATH:/path/to/dir

ex. export PATH=$PATH:/usr/local/packer

****
Also depending on what you're doing, you also may want to symlink to binaries:

  cd /usr/bin
  sudo ln -s /path/to/binary binary-name
****


---------------------------
4. Sourcing the Packer binary

Note that this will not automatically update your path for the remainder of the session. To do this, you should run:

  source ~/.profile 
or
  source ~/.bash_profile


------------------------------
5.Create symlink to Packer
**Note: RedHat/CentOS systems already includes a program called packer, that's why we would need to type out the full path each time you run a command**
        Symlink resolves this. Proper use of command is: "packer.io"

  check what "packer" is in use:
    which -a packer  
    

  sudo ln -s /usr/local/packer /usr/local/bin/packer.io


------------------------------
Packer in use:

base commands:



1.



