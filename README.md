FlightGear-CentOS
=================

Script to get FlightGear to build on CentOS (6+)

This is an updated version of the script:

http://www.gitorious.org/fg/fgmeta/blobs/raw/master/download_and_compile.sh

to allow building Flight Gear from source on CentOS 6.

This was tested on CentOS 6.3 (64 bit) with current master of FlightGear 
as of 2013-1-30 (before 2.10.0 release).


How to use
==========

Make sure you have 12GB or more of disk space.

Download download_and_compile_cento6.sh file into an empty folder.

Make it executable:

   $ chmod a+x download_and_compile_cento6.sh

Run the script:

   $ ./download_and_compile_cento6.sh


Script should create a ./run_fgfs.sh script. Run that to run latest FlightGear.


Caveats
=======


Not all components of FlightGear build. Some optional components such as:


  * FGRUN
  * FGCOM
  * FGX
  * ATLAS

don't build. But the game can be run without them.


If the original download_and_compile.sh script gets updated, might have to apply the included centos6.patch to it to generate an updated download_and_compile_centos6.sh script.


How To Update Script
====================

This script is just a patched version of the original script.

http://www.gitorious.org/fg/fgmeta/blobs/raw/master/download_and_compile.sh

The patch was generated with:


    $ diff -u <original.sh> <updated.sh> > centos6.patch

To apply the patch to the original script to get the updated version to build on CentOS 6 use:


    $ patch <original.sh> -i centos6.patch -o <updated.sh>


