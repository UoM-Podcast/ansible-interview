1. Change directory into `/home/interview/`

2. Edit the file `/home/interview/test.conf`
  * visually, find Line 14. Under `[agent]`.  `name             = 'pyca'`
  * Change the `name` value from `pyca` to your name in the format `firstname-lastname`
  * visually, find Line 199. Under `[logging]`.  `#syslog           = False`
  * Uncomment the line
  * Change the value from `False` to `True`

3. What is the assigned IP address of the local computer you are using in this test ______________?

4. You need to establish a remote computer is up and can be contacted over the Network. From the command line, write a simple command to contact the remote computer and execute it in the command prompt. The remote computer DNS address is interview1.x.x.x

5. Using `ssh` (`scp`), copy `/home/interview/test.conf`  onto the remote computer above. 
  * It should be copied to interview1.x.x.x/home/ubuntu/test.conf. 
  * Private keyfile located at `~/.ssh/interview.pem` on the **local** computer
  * username is `ubuntu`. 
  * Note you cannot connect to the remote computer via ssh with a password. Must be SSH key only.

6. Now using `ssh`, open an interactive SSH connection to the remote computer.
   * remote computer located at interview1.x.x.x.
   * Private keyfile located at `~/.ssh/interview.pem` 
   * remote computer username is `ubuntu`

7. (optional) List the current directory files on the remote computer you are now on. You will see `test.conf` from above.

8. Rename `test.conf` to `pyca.conf`. Assumption made you are in `/home/ubuntu`.

9. Move `pyca.conf` to `/home/ubuntu/pyca/etc/pyca.conf`. Note this replaces the existing `pyca.conf`.

10. Change directory to `/home/ubuntu/pyca/`

11. There is a script `start.sh`. change its permissions to be **executable**.

12. Execute (run) the script `start.sh` from the command line.

13.You should see an error message on the command. Don't worry, that's OK!
This application was configured, installed and working in the past. 
Using the error and the documentation for the application here: [link](https://github.com/opencast/pyCA#installation) try to resolve the error when executing `start.sh`. 
   * Note ubuntu is based on debian
   * Note installation configuration for the remote computer is here: [link](https://github.com/UoM-Podcast/ansible-interview/blob/045303e485f89fb17db00a13d7fcc1a5f77ae2ff/roles/pi/tasks/main.yml#L17).
