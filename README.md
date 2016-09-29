Because the Central's NFS storage is a bit flaky.


We now make a note of this in the system log, for future aggregation and analysis work.

Deployment: Copy nfs-checker into /usr/local/sbin/nfs-checker

* chmod +x that
* crontab -e, as root 
* */10 * * * * /usr/local/sbin/nfs-checker


