## Tutorial URL
My inspire from https://developer.hashicorp.com/consul/tutorials/docker/docker-compose-datacenter

TL;DR:
1. Clone this repository
2. This include 3 Servers and 1 Client
3. Create the bootstrap token
-  $docker exec -it consul-server1 /bin/sh
-  $consul acl bootstrap
4. The SecretID is the ACL token used to authenticate API and CLI requests.
5. Input your ACL token after generate like "7eb096e1-9c97-17dc-249b-1e187492c22f"
6. Add the agent token to all Consul agents
- $export CONSUL_HTTP_TOKEN=7eb096e1-9c97-17dc-249b-1e187492c22f
- $consul acl set-agent-token agent "7eb096e1-9c97-17dc-249b-1e187492c22f"
7. Message ACL token "agent" set successfully when complete
8. Enjoy your config Consul and enable ACL and login to UI http://localhost:8500/ui/dc1/acls/roles with token (7eb096e1-9c97-17dc-249b-1e187492c22f)
