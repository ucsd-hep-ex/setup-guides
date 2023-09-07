# Instructions for Google Cloud

- [Instructions for Google Cloud](#instructions-for-google-cloud)
  - [Virtual Machines (VM)](#virtual-machines-vm)
      - [Creating VM instances](#creating-vm-instances)
      - [Accessing VM instances](#accessing-vm-instances)
      - [Using VM instances](#using-vm-instances)
    - [Specific image instructions](#specific-image-instructions)
      - [kansal-image-2](#kansal-image-2)


## Virtual Machines (VM)

#### Creating VM instances

1. Go to `Compute Engine -> VM Instances`
2. Choose resources (CPU, GPU etc.)
3. Choose a disk image, you can either:
   1. Start from a standard image such as Ubuntu
   2. Start from a custom image we've made, such as `kansal-image-2` which has cuda and PyTorch installed. You can also [make your own image](https://cloud.google.com/compute/docs/images/create-delete-deprecate-private-images) and use that.
4. Select 'Allow HTTP traffic' and 'Allow HTTPS traffic'.
5. Create the image.


#### Accessing VM instances

Follow Nhan's instructions here https://fastml.slack.com/files/T6RPRPG92/FL217F4RG?origin_team=T6RPRPG92. You can find your instance's IP address on the VM Instances page.


#### Using VM instances

Some notes for using them.

- Can be used just like a standard server you `ssh` into.
- **Remember to shut them down if you are not using them**
  - `Compute Engine -> VM Instances -> <your instance name>` and click `Shutdown`. 
  - The instance state will be saved so you can continue from where you left off if you want to start it again.
- You can leave a process running and exit the instance by using, for example, [nohup](https://www.computerhope.com/unix/unohup.htm) or [screen](https://www.computerhope.com/unix/screen.htm).
- You can start an http server to access your server files from your browser using `python -m http.server`, which can be run in the background with screen or nohup. (e.g. `screen -d -m python3 -m http.server 80`)

### Specific image instructions

#### kansal-image-2

1. Switch to user with `su user` and the home directory `/app/`.
2. You may need to add miniconda to your path: `export PATH="/home/user/miniconda3/bin:$PATH"`
3. Go nuts.
