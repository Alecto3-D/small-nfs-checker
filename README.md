Background:

We rent some storage that is made available via NFS. We have autofs setup to mount it anytime a process needs that directory.
The NFS mount does occasionally become stale, so it has to be forcibly unmounted. To make sure the checking process itself doesn't get hungup, we set a one second timeout on stat.


logger dumps a note of this into the system log, for future aggregation and analysis work.

Deployment: Copy nfs-checker into /usr/local/sbin/nfs-checker

* chmod +x that
* crontab -e, as root 
* */10 * * * * /usr/local/sbin/nfs-checker
