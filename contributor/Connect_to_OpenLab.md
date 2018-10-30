# Connect to OpenLab

Follow the steps below to Connect the OpenLab:

* OpenLab maintainer will submit an issue to target project that plan to connect OpenLab, let target project maintainers know what we want to do, and discuss some details, looks like: [gophercloud Issue 592](https://github.com/gophercloud/gophercloud/issues/592)
* If the above issue is approved, OpenLab maintainer will commit a pull request to target project, **.zuul.yaml** will be included in PR, that define which CI jobs will run, looks like: [gophercloud PR 593](https://github.com/gophercloud/gophercloud/pull/593)
* Target project maintainer should install **TheOpenLab-CI** [github APP](https://github.com/apps/theopenlab-ci), so that OpenLab CI system and target project can communicate with each other, **TheOpenLab-CI** github APP only require basic permissions to update check status and commit test result log URL in PR comments, you can see permission details in APP installation web page.
