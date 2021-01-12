# kitchen-footloose
an example of plugging footloose into a CI harness to test system configuration compliance across containers/micro-vms.

intially based on a couple of hacks to merege the configs between these two tools:

https://github.com/weaveworks/footloose <br />
https://kitchen.ci

uses bundler to install and run

https://bundler.io

and docker (footloose on mac) or ignite as a backend:

http://docker.io <br />
https://github.com/weaveworks/ignite

also using the dev-sec material to validate runs against the ignite containers/VMs:

https://github.com/dev-sec/ansible-collection-hardening/tree/master/roles/os_hardening <br />
https://github.com/dev-sec/linux-baseline

## Problem

interesting because hacking to do vm type things in containers can be problematic. 
micro-vm's could pose a solution to linux cross platform/distro/version type testing if they were a first class citizen via kitchen driver. 

## Usage

```
bundler install --local
```

All kitchen commands work natively under bundler including login and referencing nodes y wildcarded substrings:

```
bundle exec kitchen list
bundle exec kitchen create
bundle exec kitchen login ubuntu
bundle exec kitchen test
```
