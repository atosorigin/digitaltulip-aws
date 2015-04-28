# digitaltulip-aws
Digital Tulip AWS provisioning

The project will create an infrastructure inside AWS, assuming it is being run in an environment with the ansible installed and AWS_KEY and AWS_SECRET set.

It will deploy to the EU Ireland region. There are two main scripts 

aws_provision which will create the whole environment
aws_setup which will add deployment keys and configure the localhosts so the name resolution can occur. Both can run in the following way

ansible-playbook -i plugins/inventory aws_provision.yml --extra-vars "env=dev"
ansible-playbook -i plugins/inventory aws_setup.yml --extra-vars "env=dev"

The extra var represents the name of the environment. This can be anything, it allows us to distinguish between different DigitalTulip Environments