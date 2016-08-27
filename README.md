# Packer

What Is Packer?

Packer is an open source tool for creating identical machine images for multiple platforms from a single source configuration. Packer is lightweight, runs on every major operating system, and is highly performant, creating machine images for multiple platforms in parallel. Packer does not replace configuration management like Chef or Puppet. In fact, when building images, Packer is able to use tools like Chef or Puppet to install software onto the image.

A machine image is a single static unit that contains a pre-configured operating system and installed software which is used to quickly create new running machines. Machine image formats change for each platform. Some examples include AMIs for EC2, VMDK/VMX files for VMware, OVF exports for VirtualBox, etc.

https://www.packer.io/intro/


# installation
```
$mkdir packer
$cd packer
$ wet https://releases.hashicorp.com/packer/0.9.0/packer_0.9.0_linux_386.zip
$unzip packer_0.9.0_linux_386.zip
$mv packer /usr/bin
$ packer --version
0.9.0
```

# example1.json
```
In this example we are just create a aws AMI [ cloning a existing ] aws ubuntu t2.micro ami

Command to execute the example1.json  [ replace aws access key and secret key with your account details ]

$ packer build \
    -var 'aws_access_key=TTRETDSFDFSDFDSFDSFDSFD' \
    -var 'aws_secret_key=Ytrtretret4654654654654regrgtretret' \
    example.json
