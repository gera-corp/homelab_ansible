# homelab_ansible

```bash
ansible-playbook -i inventories/home playbooks/vault/playbook_vault_server.yaml -K
```

```bash
ansible-playbook -i inventories/home playbooks/consul/playbook_consul_server.yaml -K --extra-vars "vault_token="
ansible-playbook -i inventories/home playbooks/consul/playbook_consul_client.yaml -K
```

```bash
ansible-playbook -i inventories/home playbooks/nomad/playbook_nomad_server-client.yaml -K
ansible-playbook -i inventories/home playbooks/nomad/playbook_nomad_server.yaml -K --extra-vars "vault_token="
ansible-playbook -i inventories/home playbooks/nomad/playbook_nomad_client.yaml -K
```