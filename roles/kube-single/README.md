kube-single
=========

Run a basic single-node Kubernetes (non-)cluster

Requirements
------------

You should use at least t2.medium -- a minimum of two CPU cores are required.

Role Variables
--------------

helm_version is set by default to the latest version at the time of this
writing in defaults/main.yml

Dependencies
------------

The jenkins helm chart comes from the "oit" branch of

https://bitbucket.org/kingdonb/helm-jenkins-chart.git

You should read `my_deploy_script` and set PUBLIC_IP variable appropriately.
Undo if necessary with `my_cleanup_script`.  It will prompt you to delete
`/data/jenkins` manually because this has the potential to lose your data.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: kube_master
      gather_facts: True
        roles:
          - kube-single

License
-------

Apache
