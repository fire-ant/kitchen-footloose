# kitchen-footloose
an example of plugging footloose into a CI harness to test system configuration compliance across containers/micro-vms.

intially based on a couple of hacks to merege the configs between these two tools:

https://github.com/weaveworks/footloose
https://kitchen.ci

uses bundler to install and run

https://bundler.io


and docker (footloose on mac) or ignite as a backend:

http://docker.io
https://github.com/weaveworks/ignite

interesting because hacking to do vm type things in containers can be problematic. 
micro-vm's could pose a solution to linux cross platform/distro/version type testing if they were a first class citizen via kitchen driver.

