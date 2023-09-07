# Fermilab LPC Environment Setup

**Important!** Go through the tutorials at the [LPC Computing](https://lpc.fnal.gov/computing/) website for getting an account, connecting to the LPC, EOS management and more!

- [Fermilab LPC Environment Setup](#fermilab-lpc-environment-setup)
  - [Disk space](#disk-space)
    - [~/.cache](#cache)
    - [VSCode Remote SSH](#vscode-remote-ssh)

## Disk space

Your home directory (`~` or `/uscms/home/<username>`) only has 2GB of disk space. **This means you should install conda / mamba, CMSSW releases, VSCode remote servers, work repositories etc. in your `~/nobackup` directory (200GB disk space)!**. See https://uscms.org/uscms_at_work/computing/setup/diskusage.shtml.

Some other tricks:

### ~/.cache

The `~/.cache` directory can sometimes fill up the home directory. To avoid this you can move it into `~/nobackup` and create a ["symbolic link"](https://linuxize.com/post/how-to-create-symbolic-links-in-linux-using-the-ln-command/) to it:

```bash
cd ~
mv .cache nobackup/
ln -s nobackup/.cache .cache
```

### VSCode Remote SSH

To use VSCode on LPC with the `remote-ssh` plugin, you need to install it in the `nobackup` directory. See https://stackoverflow.com/questions/62613523/how-to-change-vscode-server-directory/70979632#70979632.

**TODO**: more detailed instructions.