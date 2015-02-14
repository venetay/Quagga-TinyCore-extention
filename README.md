# Install in TinyCore Linux 

Place the .tcz files to /mnt/sda1/tce/optional 

Add quagga_rfc6506.tcz to /mnt/sda1/tce/onboot.lst 

Add to /opt/bootlocal.sh 	

/usr/local/sbin/zebra -u root -d -A 127.0.0.1 -i /usr/local/var/quagga/zebra.pid -f /usr/local/etc/quagga/zebra.conf
/usr/local/sbin/ospfd -u root -d -A 127.0.0.1 -i /usr/local/var/quagga/ospfd.pid -f /usr/local/etc/quagga/ospfd.conf
/usr/local/sbin/ospf6d -u root -d -A 127.0.0.1 -i /usr/local/var/quagga/ospf6d.pid -f /usr/local/etc/quagga/ospf6d.conf
/usr/local/sbin/bgpd -u root -d -A 127.0.0.1 -i /usr/local/var/quagga/bgpd.pid -f /usr/local/etc/quagga/bgpd.conf

The files in /usr/local/sbin/\* are symlinks to /tmp/tcloop/quagga_rfc6506/usr/local/sbin/\*

The files in /usr/local/lib/\* are symlinks to /tmp/tcloop/quagga_rfc6506/usr/local/libs/\* 
