This is a fork of: https://github.com/NanoHttpd/nanohttpd

Added branches:

* **nanohttpd-project-2.3.1.1:**
  Based the upstream tag `nanohttpd-project-2.3.1` which fixes an Android closeguard warning that
  occurs handling GZIP encoding and updates the version to 2.3.1.1.
* **nanohttpd-project-2.3.1.2:**
  Based on `nanohttpd-project-2.3.1.2`, this branch avoids a long reverse DNS query on certain
  routers when they are disconnected from the internet (notably some Tp-Link models). The reverse
  DNS query would happen whenever a client connects to the server but the result of the query is
  unused. The call to `InetAddress#getHostName()` is removed, as in the upstream commit cd37235.

Version 2.3.1.2 is deployed to Clovers artifactory here:
https://artifactory.corp.clover.com/artifactory/webapp/#/artifacts/browse/tree/General/libs-release-local/org/nanohttpd/nanohttpd/2.3.1.2/nanohttpd-2.3.1.2.jar.
There is no automated way to deploy this repository to artifactory. It must be built and deployed
manually.
