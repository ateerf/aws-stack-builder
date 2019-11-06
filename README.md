Sinatra Application
---------------------

An [Ansible](https://www.ansible.com/) playbook for building [Sinatra DSL](http://sinatrarb.com/) architectures on [AWS](https://aws.amazon.com/) using CloudFormation stacks.

Installation
------------

- Either clone AWS CLoudFormation Stack Builder `git clone https://github.com/ateerf/aws-stack-builder.git` or download the [released versions](https://github.com/ateerf/aws-stack-builder/releases)
- Install the following required tools:
  * [Ansible](https://www.ansible.com/) version 2.7.5 or later
  * [Python](https://www.python.org/downloads/) version 2.7.x

Usage
-----
- Set up the required [AWS Infrastructure]
- Set up EC2 Instance
- Install latest versions of Ruby, Bundle and sinatra


### Stack Manager

Create Stack Manager stacks:

 ansible-playbook -v provisioners/main.yaml -i conf/hosts --extra-vars "stack_prefix=[REAGroup-StackName] key_name=[EC2KeyPairName]"

e.g ansible-playbook -v provisioners/main.yaml -i conf/hosts --extra-vars "stack_prefix=[REAGroup-Test01] key_name=[MyKP]"
