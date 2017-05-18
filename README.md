### Ansible Kube Connection testing repo


All testing was done against OpenShift but using kube apis...so it should work.

There is a python-based image in the repo for testing.
```
oc new-app https://github.com/jcpowermac/ansible-kube-connect-test --context-dir python
```

Get the bits...
```
virtualenv kube
source kube/bin/activate
pip install kubernetes
git clone git@github.com:jcpowermac/ansible
cd ansible
git checkout kube
source hacking/env-setup

```

Example
```
ansible-playbook -vvvv -i ansible-kube-connect-test-1-d364v, site.yml
```


