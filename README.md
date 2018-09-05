# openshift-heat
Heat templates for building out an OpenShift infrastructure

This is a simple set of heat templates that can be used to build out
the instances required for an OpenShift deployment.  These instances
can then be automated via Ansible.

The main template is [templates/ocp.yaml](templates/ocp.yaml). It includes
resource definitions for the master, infrastructure node, and
application node instance type.

An example environment file [environment.yaml](environment.yaml) is at
the top level directory. To use these templates, edit that file to suit your needs and run:

```
openstack stack create -e environment.yaml -t templates/ocp.yaml ocp
```
