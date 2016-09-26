Because the Central's NFS storage is a bit flaky.

We had this running via cronjob on chalmers only:

but it also now on otto, to watch over pipeline and Paul's homedir, and marge for the gemma backup

We now make a note of this in the system log, for future aggregation and analysis work.

Deployment: Copy nfs-checker into /usr/local/sbin/nfs-checker
 chmod +x that
 crontab -e, as root
 */10 * * * * /usr/local/sbin/nfs-checker


