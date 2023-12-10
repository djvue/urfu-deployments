```zsh
ansible-lint --offline -c ansible-lint.yaml -p playbooks/*.yaml

ansible -i env.yaml -i inventory prod -m debug -a "var=hostvars[inventory_hostname]"

ansible -i env.yaml -i inventory prod -m ping

ansible-playbook -i env.yaml -i inventory playbooks/deploy_m1.yaml  --extra-vars image_tag=main
```

## See
- https://ansible-lint.readthedocs.io/
- https://docs.ansible.com/ansible/latest/collections/amazon/aws/s3_object_module.html#ansible-collections-amazon-aws-s3-object-module
- https://docs.ansible.com/ansible/latest/collections/community/aws/s3_sync_module.html
- https://docs.ansible.com/ansible/latest/collections/community/general/archive_module.html
- https://docs.ansible.com/ansible/latest/collections/ansible/builtin/unarchive_module.html
- https://docs.ansible.com/ansible/latest/collections/community/general/mail_module.html

Запустить на хосте
```bash
sudo usermod -aG docker $(whoami)
```
