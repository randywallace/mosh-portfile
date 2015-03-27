### Steps to install

* grab this repo and put it somewhere
* Add the root of this repo to your macports sources via https://guide.macports.org/chunked/development.local-repositories.html
* run ```[sudo] port sync```
* see the available versions via ```[sudo] port search mosh```
  * this repo will override the upstream portfile with a version like this ```@1.2.4-20150327```
* If you're satisfied, install it: ```[sudo] port install mosh```
* Check and make absolute sure you got this version
  * run ```mosh --version```
    * you should see something like ```mosh 1.2.4-20150327-c6cd99ba971123aa4072d3ab8466c3d2467db9bd```
    * **not** ```mosh 1.2.4a```
* enjoy!

Note that any issues you have (if it builds/installs correctly) should be directed to https://github.com/keithw/mosh

I would recommend when posting an issue to include the commit hash from ```mosh --version``` in your report.

### Steps to get updated portfile

* run ```[sudo] port selfupdate && [sudo] port upgrade mosh```
  * This will run a git pull of your working copy of this repo

### Rolling back

* ```[sudo] port installed mosh```
* ```[sudo] port activate @VERSION``` where VERSION is one of the listed installed versions
* Remove local source from macports sources file
* ```[sudo] port selfupdate``` to remove this repo completely

### Contributing

I may or may not update this repo depending on whether or not I see somthing useful to me get merged into the main mosh repo.
Feel free to submit a PR if you make an update you think is worthy, and I'll likely merge it without a lot of fanfare
if it looks good to me under the assumption that you knew what you were doing and tested appropriately.

If you just want to increment to the latest commit, update the ```git.branch``` variable in the Portfile and increment the revision number to the current date.  This will make it easy to rollback in macports if necessary.


