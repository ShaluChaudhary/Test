C:\HashiCorp\BOX>dir
 Volume in drive C is Local Disk
 Volume Serial Number is C8BE-FDEC

 Directory of C:\HashiCorp\BOX

02-12-2018  09:37    <DIR>          .
02-12-2018  09:37    <DIR>          ..
02-12-2018  09:38    <DIR>          .vagrant
02-12-2018  13:37                69 Vagrantfile
               1 File(s)             69 bytes
               3 Dir(s)   7,363,497,984 bytes free

C:\HashiCorp\BOX>vagrant ssh
VM must be running to open SSH connection. Run `vagrant up`
to start the virtual machine.

C:\HashiCorp\BOX>vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Checking if box 'centos/7' is up to date...
==> default: Clearing any previously set forwarded ports...
==> default: Vagrant has detected a configuration issue which exposes a
==> default: vulnerability with the installed version of VirtualBox. The
==> default: current guest is configured to use an E1000 NIC type for a
==> default: network adapter which is vulnerable in this version of VirtualBox.
==> default: Ensure the guest is trusted to use this configuration or update
==> default: the NIC type using one of the methods below:
==> default:
==> default:   https://www.vagrantup.com/docs/virtualbox/configuration.html#default-nic-type
==> default:   https://www.vagrantup.com/docs/virtualbox/networking.html#virtualbox-nic-type
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
==> default: Forwarding ports...
    default: 22 (guest) => 2222 (host) (adapter 1)
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
    default: No guest additions were detected on the base box for this VM! Guest
    default: additions are required for forwarded ports, shared folders, host only
    default: networking, and more. If SSH fails on this machine, please install
    default: the guest additions and repackage the box to continue.
    default:
    default: This is not an error message; everything may continue to work properly,
    default: in which case you may ignore this message.
==> default: Rsyncing folder: /cygdrive/c/HashiCorp/BOX/ => /vagrant
==> default: Machine already provisioned. Run `vagrant provision` or use the `--provision`
==> default: flag to force provisioning. Provisioners marked to run always will still run.

C:\HashiCorp\BOX>vagrant ssh
Last login: Sun Dec  2 09:52:57 2018 from 10.0.2.2
[vagrant@localhost ~]$ git clone https://github.com/ShaluChaudhary/Test.git
-bash: git: command not found
[vagrant@localhost ~]$ sudo yum list git
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: centos.excellmedia.net
 * extras: centos.excellmedia.net
 * updates: centos.excellmedia.net
Available Packages
git.x86_64                                           1.8.3.1-14.el7_5                                            updates
[vagrant@localhost ~]$ sudo rpm -ql git
package git is not installed
[vagrant@localhost ~]$ sudo yum install git -y
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: centos.excellmedia.net
 * extras: centos.excellmedia.net
 * updates: centos.excellmedia.net
Resolving Dependencies
--> Running transaction check
---> Package git.x86_64 0:1.8.3.1-14.el7_5 will be installed
--> Processing Dependency: perl-Git = 1.8.3.1-14.el7_5 for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl >= 5.008 for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(warnings) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(vars) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(strict) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(lib) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(Term::ReadKey) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(Git) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(Getopt::Long) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(File::stat) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(File::Temp) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(File::Spec) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(File::Path) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(File::Find) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(File::Copy) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(File::Basename) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(Exporter) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: perl(Error) for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: /usr/bin/perl for package: git-1.8.3.1-14.el7_5.x86_64
--> Processing Dependency: libgnome-keyring.so.0()(64bit) for package: git-1.8.3.1-14.el7_5.x86_64
--> Running transaction check
---> Package libgnome-keyring.x86_64 0:3.12.0-1.el7 will be installed
---> Package perl.x86_64 4:5.16.3-292.el7 will be installed
--> Processing Dependency: perl-libs = 4:5.16.3-292.el7 for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Socket) >= 1.3 for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Scalar::Util) >= 1.10 for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl-macros for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl-libs for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(threads::shared) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(threads) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(constant) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Time::Local) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Time::HiRes) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Storable) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Socket) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Scalar::Util) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Pod::Simple::XHTML) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Pod::Simple::Search) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Filter::Util::Call) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: perl(Carp) for package: 4:perl-5.16.3-292.el7.x86_64
--> Processing Dependency: libperl.so()(64bit) for package: 4:perl-5.16.3-292.el7.x86_64
---> Package perl-Error.noarch 1:0.17020-2.el7 will be installed
---> Package perl-Exporter.noarch 0:5.68-3.el7 will be installed
---> Package perl-File-Path.noarch 0:2.09-2.el7 will be installed
---> Package perl-File-Temp.noarch 0:0.23.01-3.el7 will be installed
---> Package perl-Getopt-Long.noarch 0:2.40-3.el7 will be installed
--> Processing Dependency: perl(Pod::Usage) >= 1.14 for package: perl-Getopt-Long-2.40-3.el7.noarch
--> Processing Dependency: perl(Text::ParseWords) for package: perl-Getopt-Long-2.40-3.el7.noarch
---> Package perl-Git.noarch 0:1.8.3.1-14.el7_5 will be installed
---> Package perl-PathTools.x86_64 0:3.40-5.el7 will be installed
---> Package perl-TermReadKey.x86_64 0:2.30-20.el7 will be installed
--> Running transaction check
---> Package perl-Carp.noarch 0:1.26-244.el7 will be installed
---> Package perl-Filter.x86_64 0:1.49-3.el7 will be installed
---> Package perl-Pod-Simple.noarch 1:3.28-4.el7 will be installed
--> Processing Dependency: perl(Pod::Escapes) >= 1.04 for package: 1:perl-Pod-Simple-3.28-4.el7.noarch
--> Processing Dependency: perl(Encode) for package: 1:perl-Pod-Simple-3.28-4.el7.noarch
---> Package perl-Pod-Usage.noarch 0:1.63-3.el7 will be installed
--> Processing Dependency: perl(Pod::Text) >= 3.15 for package: perl-Pod-Usage-1.63-3.el7.noarch
--> Processing Dependency: perl-Pod-Perldoc for package: perl-Pod-Usage-1.63-3.el7.noarch
---> Package perl-Scalar-List-Utils.x86_64 0:1.27-248.el7 will be installed
---> Package perl-Socket.x86_64 0:2.010-4.el7 will be installed
---> Package perl-Storable.x86_64 0:2.45-3.el7 will be installed
---> Package perl-Text-ParseWords.noarch 0:3.29-4.el7 will be installed
---> Package perl-Time-HiRes.x86_64 4:1.9725-3.el7 will be installed
---> Package perl-Time-Local.noarch 0:1.2300-2.el7 will be installed
---> Package perl-constant.noarch 0:1.27-2.el7 will be installed
---> Package perl-libs.x86_64 4:5.16.3-292.el7 will be installed
---> Package perl-macros.x86_64 4:5.16.3-292.el7 will be installed
---> Package perl-threads.x86_64 0:1.87-4.el7 will be installed
---> Package perl-threads-shared.x86_64 0:1.43-6.el7 will be installed
--> Running transaction check
---> Package perl-Encode.x86_64 0:2.51-7.el7 will be installed
---> Package perl-Pod-Escapes.noarch 1:1.04-292.el7 will be installed
---> Package perl-Pod-Perldoc.noarch 0:3.20-4.el7 will be installed
--> Processing Dependency: perl(parent) for package: perl-Pod-Perldoc-3.20-4.el7.noarch
--> Processing Dependency: perl(HTTP::Tiny) for package: perl-Pod-Perldoc-3.20-4.el7.noarch
---> Package perl-podlators.noarch 0:2.5.1-3.el7 will be installed
--> Running transaction check
---> Package perl-HTTP-Tiny.noarch 0:0.033-3.el7 will be installed
---> Package perl-parent.noarch 1:0.225-244.el7 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

========================================================================================================================
 Package                              Arch                 Version                          Repository             Size
========================================================================================================================
Installing:
 git                                  x86_64               1.8.3.1-14.el7_5                 updates               4.4 M
Installing for dependencies:
 libgnome-keyring                     x86_64               3.12.0-1.el7                     base                  109 k
 perl                                 x86_64               4:5.16.3-292.el7                 base                  8.0 M
 perl-Carp                            noarch               1.26-244.el7                     base                   19 k
 perl-Encode                          x86_64               2.51-7.el7                       base                  1.5 M
 perl-Error                           noarch               1:0.17020-2.el7                  base                   32 k
 perl-Exporter                        noarch               5.68-3.el7                       base                   28 k
 perl-File-Path                       noarch               2.09-2.el7                       base                   26 k
 perl-File-Temp                       noarch               0.23.01-3.el7                    base                   56 k
 perl-Filter                          x86_64               1.49-3.el7                       base                   76 k
 perl-Getopt-Long                     noarch               2.40-3.el7                       base                   56 k
 perl-Git                             noarch               1.8.3.1-14.el7_5                 updates                54 k
 perl-HTTP-Tiny                       noarch               0.033-3.el7                      base                   38 k
 perl-PathTools                       x86_64               3.40-5.el7                       base                   82 k
 perl-Pod-Escapes                     noarch               1:1.04-292.el7                   base                   51 k
 perl-Pod-Perldoc                     noarch               3.20-4.el7                       base                   87 k
 perl-Pod-Simple                      noarch               1:3.28-4.el7                     base                  216 k
 perl-Pod-Usage                       noarch               1.63-3.el7                       base                   27 k
 perl-Scalar-List-Utils               x86_64               1.27-248.el7                     base                   36 k
 perl-Socket                          x86_64               2.010-4.el7                      base                   49 k
 perl-Storable                        x86_64               2.45-3.el7                       base                   77 k
 perl-TermReadKey                     x86_64               2.30-20.el7                      base                   31 k
 perl-Text-ParseWords                 noarch               3.29-4.el7                       base                   14 k
 perl-Time-HiRes                      x86_64               4:1.9725-3.el7                   base                   45 k
 perl-Time-Local                      noarch               1.2300-2.el7                     base                   24 k
 perl-constant                        noarch               1.27-2.el7                       base                   19 k
 perl-libs                            x86_64               4:5.16.3-292.el7                 base                  688 k
 perl-macros                          x86_64               4:5.16.3-292.el7                 base                   43 k
 perl-parent                          noarch               1:0.225-244.el7                  base                   12 k
 perl-podlators                       noarch               2.5.1-3.el7                      base                  112 k
 perl-threads                         x86_64               1.87-4.el7                       base                   49 k
 perl-threads-shared                  x86_64               1.43-6.el7                       base                   39 k

Transaction Summary
========================================================================================================================
Install  1 Package (+31 Dependent packages)

Total download size: 16 M
Installed size: 59 M
Downloading packages:
No Presto metadata available for base
updates/7/x86_64/prestodelta                                                                     | 679 kB  00:00:02
warning: /var/cache/yum/x86_64/7/base/packages/libgnome-keyring-3.12.0-1.el7.x86_64.rpm: Header V3 RSA/SHA256 Signature, key ID f4a80eb5: NOKEY
Public key for libgnome-keyring-3.12.0-1.el7.x86_64.rpm is not installed
(1/32): libgnome-keyring-3.12.0-1.el7.x86_64.rpm                                                 | 109 kB  00:00:01
(2/32): perl-Carp-1.26-244.el7.noarch.rpm                                                        |  19 kB  00:00:01
(3/32): perl-Error-0.17020-2.el7.noarch.rpm                                                      |  32 kB  00:00:00
(4/32): perl-Exporter-5.68-3.el7.noarch.rpm                                                      |  28 kB  00:00:00
(5/32): perl-File-Path-2.09-2.el7.noarch.rpm                                                     |  26 kB  00:00:00
(6/32): perl-Filter-1.49-3.el7.x86_64.rpm                                                        |  76 kB  00:00:00
(7/32): perl-Getopt-Long-2.40-3.el7.noarch.rpm                                                   |  56 kB  00:00:01
(8/32): perl-Encode-2.51-7.el7.x86_64.rpm                                                        | 1.5 MB  00:00:07
(9/32): perl-File-Temp-0.23.01-3.el7.noarch.rpm                                                  |  56 kB  00:00:06
(10/32): perl-PathTools-3.40-5.el7.x86_64.rpm                                                    |  82 kB  00:00:01
(11/32): perl-Pod-Escapes-1.04-292.el7.noarch.rpm                                                |  51 kB  00:00:00
(12/32): perl-Pod-Perldoc-3.20-4.el7.noarch.rpm                                                  |  87 kB  00:00:00
(13/32): perl-Pod-Simple-3.28-4.el7.noarch.rpm                                                   | 216 kB  00:00:01
(14/32): perl-Pod-Usage-1.63-3.el7.noarch.rpm                                                    |  27 kB  00:00:00
(15/32): perl-Scalar-List-Utils-1.27-248.el7.x86_64.rpm                                          |  36 kB  00:00:01
(16/32): perl-HTTP-Tiny-0.033-3.el7.noarch.rpm                                                   |  38 kB  00:00:08
(17/32): perl-Socket-2.010-4.el7.x86_64.rpm                                                      |  49 kB  00:00:01
(18/32): perl-TermReadKey-2.30-20.el7.x86_64.rpm                                                 |  31 kB  00:00:00
(19/32): perl-Text-ParseWords-3.29-4.el7.noarch.rpm                                              |  14 kB  00:00:00
(20/32): perl-Time-HiRes-1.9725-3.el7.x86_64.rpm                                                 |  45 kB  00:00:00
(21/32): perl-Time-Local-1.2300-2.el7.noarch.rpm                                                 |  24 kB  00:00:00
(22/32): perl-constant-1.27-2.el7.noarch.rpm                                                     |  19 kB  00:00:00
Public key for perl-Git-1.8.3.1-14.el7_5.noarch.rpm is not installed                  ] 225 kB/s | 5.2 MB  00:00:49 ETA
(23/32): perl-Git-1.8.3.1-14.el7_5.noarch.rpm                                                    |  54 kB  00:00:14
(24/32): perl-Storable-2.45-3.el7.x86_64.rpm                                                     |  77 kB  00:00:04
(25/32): perl-macros-5.16.3-292.el7.x86_64.rpm                                                   |  43 kB  00:00:00
(26/32): perl-parent-0.225-244.el7.noarch.rpm                                                    |  12 kB  00:00:01
(27/32): perl-threads-1.87-4.el7.x86_64.rpm                                                      |  49 kB  00:00:00
(28/32): perl-podlators-2.5.1-3.el7.noarch.rpm                                                   | 112 kB  00:00:01
(29/32): perl-threads-shared-1.43-6.el7.x86_64.rpm                                               |  39 kB  00:00:00
(30/32): perl-libs-5.16.3-292.el7.x86_64.rpm                                                     | 688 kB  00:00:04
(31/32): git-1.8.3.1-14.el7_5.x86_64.rpm                                                         | 4.4 MB  00:00:30
(32/32): perl-5.16.3-292.el7.x86_64.rpm                                                          | 8.0 MB  00:00:38
------------------------------------------------------------------------------------------------------------------------
Total                                                                                   420 kB/s |  16 MB  00:00:38
Retrieving key from file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
Importing GPG key 0xF4A80EB5:
 Userid     : "CentOS-7 Key (CentOS 7 Official Signing Key) <security@centos.org>"
 Fingerprint: 6341 ab27 53d7 8a78 a7c2 7bb1 24c6 a8a7 f4a8 0eb5
 Package    : centos-release-7-5.1804.4.el7.centos.x86_64 (@koji-override-1)
 From       : /etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  Installing : 1:perl-parent-0.225-244.el7.noarch                                                                  1/32
  Installing : perl-HTTP-Tiny-0.033-3.el7.noarch                                                                   2/32
  Installing : perl-podlators-2.5.1-3.el7.noarch                                                                   3/32
  Installing : perl-Pod-Perldoc-3.20-4.el7.noarch                                                                  4/32
  Installing : 1:perl-Pod-Escapes-1.04-292.el7.noarch                                                              5/32
  Installing : perl-Text-ParseWords-3.29-4.el7.noarch                                                              6/32
  Installing : perl-Encode-2.51-7.el7.x86_64                                                                       7/32
  Installing : perl-Pod-Usage-1.63-3.el7.noarch                                                                    8/32
  Installing : 4:perl-macros-5.16.3-292.el7.x86_64                                                                 9/32
  Installing : 4:perl-libs-5.16.3-292.el7.x86_64                                                                  10/32
  Installing : perl-Storable-2.45-3.el7.x86_64                                                                    11/32
  Installing : perl-Exporter-5.68-3.el7.noarch                                                                    12/32
  Installing : perl-constant-1.27-2.el7.noarch                                                                    13/32
  Installing : perl-Time-Local-1.2300-2.el7.noarch                                                                14/32
  Installing : perl-Socket-2.010-4.el7.x86_64                                                                     15/32
  Installing : perl-Carp-1.26-244.el7.noarch                                                                      16/32
  Installing : 4:perl-Time-HiRes-1.9725-3.el7.x86_64                                                              17/32
  Installing : perl-PathTools-3.40-5.el7.x86_64                                                                   18/32
  Installing : perl-Scalar-List-Utils-1.27-248.el7.x86_64                                                         19/32
  Installing : perl-File-Temp-0.23.01-3.el7.noarch                                                                20/32
  Installing : perl-File-Path-2.09-2.el7.noarch                                                                   21/32
  Installing : perl-threads-shared-1.43-6.el7.x86_64                                                              22/32
  Installing : perl-threads-1.87-4.el7.x86_64                                                                     23/32
  Installing : perl-Filter-1.49-3.el7.x86_64                                                                      24/32
  Installing : 1:perl-Pod-Simple-3.28-4.el7.noarch                                                                25/32
  Installing : perl-Getopt-Long-2.40-3.el7.noarch                                                                 26/32
  Installing : 4:perl-5.16.3-292.el7.x86_64                                                                       27/32
  Installing : 1:perl-Error-0.17020-2.el7.noarch                                                                  28/32
  Installing : perl-TermReadKey-2.30-20.el7.x86_64                                                                29/32
  Installing : libgnome-keyring-3.12.0-1.el7.x86_64                                                               30/32
  Installing : perl-Git-1.8.3.1-14.el7_5.noarch                                                                   31/32
  Installing : git-1.8.3.1-14.el7_5.x86_64                                                                        32/32
  Verifying  : perl-HTTP-Tiny-0.033-3.el7.noarch                                                                   1/32
  Verifying  : libgnome-keyring-3.12.0-1.el7.x86_64                                                                2/32
  Verifying  : perl-threads-shared-1.43-6.el7.x86_64                                                               3/32
  Verifying  : perl-Storable-2.45-3.el7.x86_64                                                                     4/32
  Verifying  : perl-Exporter-5.68-3.el7.noarch                                                                     5/32
  Verifying  : perl-constant-1.27-2.el7.noarch                                                                     6/32
  Verifying  : perl-PathTools-3.40-5.el7.x86_64                                                                    7/32
  Verifying  : 4:perl-macros-5.16.3-292.el7.x86_64                                                                 8/32
  Verifying  : 1:perl-parent-0.225-244.el7.noarch                                                                  9/32
  Verifying  : 4:perl-5.16.3-292.el7.x86_64                                                                       10/32
  Verifying  : perl-TermReadKey-2.30-20.el7.x86_64                                                                11/32
  Verifying  : perl-File-Temp-0.23.01-3.el7.noarch                                                                12/32
  Verifying  : 1:perl-Pod-Simple-3.28-4.el7.noarch                                                                13/32
  Verifying  : perl-Time-Local-1.2300-2.el7.noarch                                                                14/32
  Verifying  : 4:perl-libs-5.16.3-292.el7.x86_64                                                                  15/32
  Verifying  : perl-Socket-2.010-4.el7.x86_64                                                                     16/32
  Verifying  : git-1.8.3.1-14.el7_5.x86_64                                                                        17/32
  Verifying  : perl-Carp-1.26-244.el7.noarch                                                                      18/32
  Verifying  : 1:perl-Error-0.17020-2.el7.noarch                                                                  19/32
  Verifying  : 4:perl-Time-HiRes-1.9725-3.el7.x86_64                                                              20/32
  Verifying  : perl-Scalar-List-Utils-1.27-248.el7.x86_64                                                         21/32
  Verifying  : 1:perl-Pod-Escapes-1.04-292.el7.noarch                                                             22/32
  Verifying  : perl-Pod-Usage-1.63-3.el7.noarch                                                                   23/32
  Verifying  : perl-Git-1.8.3.1-14.el7_5.noarch                                                                   24/32
  Verifying  : perl-Encode-2.51-7.el7.x86_64                                                                      25/32
  Verifying  : perl-Pod-Perldoc-3.20-4.el7.noarch                                                                 26/32
  Verifying  : perl-podlators-2.5.1-3.el7.noarch                                                                  27/32
  Verifying  : perl-File-Path-2.09-2.el7.noarch                                                                   28/32
  Verifying  : perl-threads-1.87-4.el7.x86_64                                                                     29/32
  Verifying  : perl-Filter-1.49-3.el7.x86_64                                                                      30/32
  Verifying  : perl-Getopt-Long-2.40-3.el7.noarch                                                                 31/32
  Verifying  : perl-Text-ParseWords-3.29-4.el7.noarch                                                             32/32

Installed:
  git.x86_64 0:1.8.3.1-14.el7_5

Dependency Installed:
  libgnome-keyring.x86_64 0:3.12.0-1.el7                   perl.x86_64 4:5.16.3-292.el7
  perl-Carp.noarch 0:1.26-244.el7                          perl-Encode.x86_64 0:2.51-7.el7
  perl-Error.noarch 1:0.17020-2.el7                        perl-Exporter.noarch 0:5.68-3.el7
  perl-File-Path.noarch 0:2.09-2.el7                       perl-File-Temp.noarch 0:0.23.01-3.el7
  perl-Filter.x86_64 0:1.49-3.el7                          perl-Getopt-Long.noarch 0:2.40-3.el7
  perl-Git.noarch 0:1.8.3.1-14.el7_5                       perl-HTTP-Tiny.noarch 0:0.033-3.el7
  perl-PathTools.x86_64 0:3.40-5.el7                       perl-Pod-Escapes.noarch 1:1.04-292.el7
  perl-Pod-Perldoc.noarch 0:3.20-4.el7                     perl-Pod-Simple.noarch 1:3.28-4.el7
  perl-Pod-Usage.noarch 0:1.63-3.el7                       perl-Scalar-List-Utils.x86_64 0:1.27-248.el7
  perl-Socket.x86_64 0:2.010-4.el7                         perl-Storable.x86_64 0:2.45-3.el7
  perl-TermReadKey.x86_64 0:2.30-20.el7                    perl-Text-ParseWords.noarch 0:3.29-4.el7
  perl-Time-HiRes.x86_64 4:1.9725-3.el7                    perl-Time-Local.noarch 0:1.2300-2.el7
  perl-constant.noarch 0:1.27-2.el7                        perl-libs.x86_64 4:5.16.3-292.el7
  perl-macros.x86_64 4:5.16.3-292.el7                      perl-parent.noarch 1:0.225-244.el7
  perl-podlators.noarch 0:2.5.1-3.el7                      perl-threads.x86_64 0:1.87-4.el7
  perl-threads-shared.x86_64 0:1.43-6.el7

Complete!
[vagrant@localhost ~]$ git clone https://github.com/ShaluChaudhary/Test.git
Cloning into 'Test'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
[vagrant@localhost ~]$ ll
total 4
drwxrwxr-x. 3 vagrant vagrant 4096 Dec  2 15:07 Test
[vagrant@localhost ~]$ cd Test
[vagrant@localhost Test]$ ll
total 4
-rw-rw-r--. 1 vagrant vagrant 6 Dec  2 15:07 README.md
[vagrant@localhost Test]$ sudo yum install gcc -y
Loaded plugins: fastestmirror
Loading mirror speeds from cached hostfile
 * base: centos.excellmedia.net
 * extras: centos.excellmedia.net
 * updates: centos.excellmedia.net
Resolving Dependencies
--> Running transaction check
---> Package gcc.x86_64 0:4.8.5-28.el7_5.1 will be installed
--> Processing Dependency: cpp = 4.8.5-28.el7_5.1 for package: gcc-4.8.5-28.el7_5.1.x86_64
--> Processing Dependency: glibc-devel >= 2.2.90-12 for package: gcc-4.8.5-28.el7_5.1.x86_64
--> Processing Dependency: libmpfr.so.4()(64bit) for package: gcc-4.8.5-28.el7_5.1.x86_64
--> Processing Dependency: libmpc.so.3()(64bit) for package: gcc-4.8.5-28.el7_5.1.x86_64
--> Running transaction check
---> Package cpp.x86_64 0:4.8.5-28.el7_5.1 will be installed
---> Package glibc-devel.x86_64 0:2.17-222.el7 will be installed
--> Processing Dependency: glibc-headers = 2.17-222.el7 for package: glibc-devel-2.17-222.el7.x86_64
--> Processing Dependency: glibc-headers for package: glibc-devel-2.17-222.el7.x86_64
---> Package libmpc.x86_64 0:1.0.1-3.el7 will be installed
---> Package mpfr.x86_64 0:3.1.1-4.el7 will be installed
--> Running transaction check
---> Package glibc-headers.x86_64 0:2.17-222.el7 will be installed
--> Processing Dependency: kernel-headers >= 2.2.1 for package: glibc-headers-2.17-222.el7.x86_64
--> Processing Dependency: kernel-headers for package: glibc-headers-2.17-222.el7.x86_64
--> Running transaction check
---> Package kernel-headers.x86_64 0:3.10.0-862.14.4.el7 will be installed
--> Finished Dependency Resolution

Dependencies Resolved

========================================================================================================================
 Package                       Arch                  Version                               Repository              Size
========================================================================================================================
Installing:
 gcc                           x86_64                4.8.5-28.el7_5.1                      updates                 16 M
Installing for dependencies:
 cpp                           x86_64                4.8.5-28.el7_5.1                      updates                5.9 M
 glibc-devel                   x86_64                2.17-222.el7                          base                   1.1 M
 glibc-headers                 x86_64                2.17-222.el7                          base                   678 k
 kernel-headers                x86_64                3.10.0-862.14.4.el7                   updates                7.1 M
 libmpc                        x86_64                1.0.1-3.el7                           base                    51 k
 mpfr                          x86_64                3.1.1-4.el7                           base                   203 k

Transaction Summary
========================================================================================================================
Install  1 Package (+6 Dependent packages)

Total download size: 31 M
Installed size: 60 M
Downloading packages:
(1/7): glibc-headers-2.17-222.el7.x86_64.rpm                                                     | 678 kB  00:00:10
(2/7): glibc-devel-2.17-222.el7.x86_64.rpm                                                       | 1.1 MB  00:00:10
(3/7): libmpc-1.0.1-3.el7.x86_64.rpm                                                             |  51 kB  00:00:01
(4/7): mpfr-3.1.1-4.el7.x86_64.rpm                                                               | 203 kB  00:00:04
(5/7): kernel-headers-3.10.0-862.14.4.el7.x86_64.rpm                                             | 7.1 MB  00:02:10
(6/7): cpp-4.8.5-28.el7_5.1.x86_64.rpm                                                           | 5.9 MB  00:02:22
(7/7): gcc-4.8.5-28.el7_5.1.x86_64.rpm                                                           |  16 MB  00:03:01
------------------------------------------------------------------------------------------------------------------------
Total                                                                                   176 kB/s |  31 MB  00:03:01
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  Installing : mpfr-3.1.1-4.el7.x86_64                                                                              1/7
  Installing : libmpc-1.0.1-3.el7.x86_64                                                                            2/7
  Installing : cpp-4.8.5-28.el7_5.1.x86_64                                                                          3/7
  Installing : kernel-headers-3.10.0-862.14.4.el7.x86_64                                                            4/7
  Installing : glibc-headers-2.17-222.el7.x86_64                                                                    5/7
  Installing : glibc-devel-2.17-222.el7.x86_64                                                                      6/7
  Installing : gcc-4.8.5-28.el7_5.1.x86_64                                                                          7/7
  Verifying  : gcc-4.8.5-28.el7_5.1.x86_64                                                                          1/7
  Verifying  : glibc-devel-2.17-222.el7.x86_64                                                                      2/7
  Verifying  : mpfr-3.1.1-4.el7.x86_64                                                                              3/7
  Verifying  : cpp-4.8.5-28.el7_5.1.x86_64                                                                          4/7
  Verifying  : glibc-headers-2.17-222.el7.x86_64                                                                    5/7
  Verifying  : libmpc-1.0.1-3.el7.x86_64                                                                            6/7
  Verifying  : kernel-headers-3.10.0-862.14.4.el7.x86_64                                                            7/7

Installed:
  gcc.x86_64 0:4.8.5-28.el7_5.1

Dependency Installed:
  cpp.x86_64 0:4.8.5-28.el7_5.1                glibc-devel.x86_64 0:2.17-222.el7  glibc-headers.x86_64 0:2.17-222.el7
  kernel-headers.x86_64 0:3.10.0-862.14.4.el7  libmpc.x86_64 0:1.0.1-3.el7        mpfr.x86_64 0:3.1.1-4.el7

Complete!
[vagrant@localhost Test]$ ll
total 4
-rw-rw-r--. 1 vagrant vagrant 6 Dec  2 15:07 README.md
[vagrant@localhost Test]$ vi file1.c
[vagrant@localhost Test]$  [New] 7L, 73C written
[vagrant@localhost Test]$ ll
total 8
-rw-rw-r--. 1 vagrant vagrant 73 Dec  2 15:25 file1.c
-rw-rw-r--. 1 vagrant vagrant  6 Dec  2 15:07 README.md
[vagrant@localhost Test]$ cat file1.c
#include <stdio.h>
int main()
{
printf (" this is file 1");
return 0;
}

[vagrant@localhost Test]$ gcc file.c
gcc: error: file.c: No such file or directory
gcc: fatal error: no input files
compilation terminated.
[vagrant@localhost Test]$ gcc file1.c
[vagrant@localhost Test]$ ./a.out
 this is file 1[vagrant@localhost Test]$
[vagrant@localhost Test]$ git config --global user.name "Shalu"
[vagrant@localhost Test]$ git config --global user.email "shalud70@gmail.com"
[vagrant@localhost Test]$ git add file1.c
[vagrant@localhost Test]$ git commit -m " first commit"
[master 66b953f]  first commit
 1 file changed, 7 insertions(+)
 create mode 100644 file1.c
[vagrant@localhost Test]$ git status
# On branch master
# Your branch is ahead of 'origin/master' by 1 commit.
#   (use "git push" to publish your local commits)
#
# Untracked files:
#   (use "git add <file>..." to include in what will be committed)
#
#       a.out
nothing added to commit but untracked files present (use "git add" to track)
[vagrant@localhost Test]$ git push -u origin master
Username for 'https://github.com': shalu
Password for 'https://shalu@github.com':
remote: Invalid username or password.
fatal: Authentication failed for 'https://github.com/ShaluChaudhary/Test.git/'
[vagrant@localhost Test]$ git push -u origin master
Username for 'https://github.com': ShaluChaudhary
Password for 'https://ShaluChaudhary@github.com':
Counting objects: 4, done.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 338 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/ShaluChaudhary/Test.git
   dbf2c36..66b953f  master -> master
Branch master set up to track remote branch master from origin.
[vagrant@localhost Test]$
