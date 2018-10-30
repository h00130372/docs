# Development Workflow

## Prerequisites
The OpenLab CI is built based on `NodePool` and `Zuul` tools of the OpenStack infrastructure. The CI Jobs definition uses Ansible playbooks. Learn more about the tools first:
* Zuul documentation is hosted on [Zuul](https://zuul-ci.org)
* NodePool documentation is hosted on [NodePool](https://zuul-ci.org/docs/nodepool/)
* Ansible documentation is hosted on [Ansible Docs](https://docs.ansible.com/)

## Working on Ocean request
The accepted test request items can be found on [TODO List](https://github.com/orgs/theopenlab/projects/1#column-1860008).
1. Pick one item you wish to work on, move it to [IN PROGRESS List](https://github.com/orgs/theopenlab/projects/1#column-1860011), edit the item to add the development plan
2. The target project of the request item should install the **OpenLab-CI** [github APP](https://github.com/apps/theopenlab-ci), so that OpenLab CI system and target project can communicate with each other. See the details on [Connect_to_OpenLab](./Connect_to_OpenLab.md)
3. Fork your own copy of the CI Job repository [openlab-zuul-jobs](https://github.com/theopenlab/openlab-zuul-jobs) to your account, develop the test job and submit a PR(Pull Request). In order to manage the test request well, please relate the request number in PR's commit message, the format like:
   
   `Related-Bug: theopenlab/ocean/issues/#number` 
4. Our development core members will review the PR, merge it if there is no error, at the meanwhile, you should contact our core members to add the target project into **main.yaml** in **zuul** node
5. Trigger to test the integration job by [Trigger Comments](./Supported_trigger_comments.md), see the [build status](http://status.openlabtesting.org/t/openlab/builds.html), click `logs` to get the log details if the job built fail, retest until all test cases success. Maybe you can find some problems of target project in the test, feel free to submit an issue to target project, relate the issue number in PR's commit message as we do on step3 
6. Close the `In Progress` item yourself or contact our development core to close it when the request test complete 

## Working on Bug
1. Bug reports for OpenLab are tracked on [bug list](https://github.com/theopenlab/openlab/issues). 
2. The merged CI job will fail due to some reasons after it has been running for some time, or if you find any other problems of OpenLab welcome to [new](https://github.com/theopenlab/openlab/issues/new) an issue
3. The governance team owner will confirm the bugs, add them to [TODO List](https://github.com/orgs/theopenlab/projects/1#column-1860008)
4. You can assign one bug from TODO list, move the item to [IN PROGRESS List](https://github.com/orgs/theopenlab/projects/1#column-1860011) 
5. Submit a PR(Pull Request), no matter where the PR submitted to, the issue number should be related in commit message. And then do the test to fix the bug
6. Close the `In Progress` item yourself or contact our development core to close it when the bug is fixed
