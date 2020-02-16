# deploy-neo4j-cluster
Ansible Playbook : Deploys a Neo4j cluster architecture

## How to use it
### 1. Create hosts file
Your host file must contains 2 groups: `cores` and `read_replicas`.

Here's an example:

    [cores]
      core1.myservers.com
      core2.myservers.com
      core3.myservers.com

    [read_replicas]
      rr1.myservers.com
      rr2.myservers.com

### 2. Change vars files
You have 2 files of variables located in `group_vars` folder:
* `all.yml`
* `cores.yml`
* `read_replicas.yml`

Please complete those files with your own values. All the variables are commented,
it explains how to fill them out.

### 3. Put the correct Neo4j file
Download the .tar.gz archive of Neo4j enterprise edition. Note down the version.
It should match with the version filled out in `all.yml`.

Move the file in : `roles/upload/neo4j-binaries/`
