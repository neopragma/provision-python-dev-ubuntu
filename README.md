# provision-python-dev-ubuntu

Provision an instance of Ubuntu Linux with software to be a Python development environment.

## Steps

The instructions assume you will provision a virtual machine with Ubuntu Linux. 

### Step 1 - Download Ubuntu iso

Open a browser and navigate to http://www.ubuntu.com. Download the iso for the version of Ubuntu desktop you want to install.

### Step 2 - Create VM

Using the virtualization product you want to use, create a VM and install Ubuntu on it. Suggest using ```pythondev``` as the administrator userid and password.

### Step 3 - Apply system updates

Start the VM and ensure it has a connection to the Internet. Apply any available system updates. Use the Software Updater icon that appears in the Unity launcher or open a Terminal and apply updates using the command line:

```shell
sudo apt-get -y update
sudo apt-get -y -f dist-upgrade
```

### Step 4 - Install git

 Install git.

```shell
sudo apt-get install git
```

### Step 5 - Clone this repo

With git installed, you can load this provisioning project on the new instance:

```shell
cd
git clone https://github.com/neopragma/provision-python-dev-ubuntu
```

### Step 6 - Run the setup script

Run the setup script.

```shell
cd ~/provision-python-dev-ubuntu
./setup
```

### Step 7 - Verify the setup

The last thing the setup script does is to run a script named verify. Check the output from verify and see if any of the installation steps failed. If so, investigate and resolve the problems. If you discover a problem with the setup script, fix it and make a pull request.
