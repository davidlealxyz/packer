export the aws private and secrete keys to your env shell variables before running

packer validate file.json
packer build -debug file.json -o- packer build  file.json

1. add a rsa.pub key to your key pairs in aws console
2. change the variables the following variables in the `packer/*.json` file:

        "ssh_keypair_name": ""  <-- the name of your keypair in aws console
        "ssh_private_key_file": <-- path to your private rsa key for that key pair

that would be the ssh key key you use will to access that machine
