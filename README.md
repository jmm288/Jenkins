# Jenkins Docker-Compose Environment
This is a functional Jenkins deployment server with containerized linux agents and integrated LDAP functionality and PHP LDAP Adamin web UI.

The Jenkins image itself is build off the provided Dockerfile.

## Requirements
1. an .ENV file with a "JENKINS_AGENT_SSH_PUBKEY" entry that passes the public key to the Jenkins server.
2. A private key credential in the Jenkins server that corresponds to the public key in the .ENV file. This way the agent can authenticate with the server.
3. If you want webhooks, notifications, and continuous deployments you'd need to get a public endpoint to access this from.

### Future updates
1. Backup LDAP files with openldap-backup, untested.
2. Terraform or Cloudformation some AWS architecture to make public instances.
