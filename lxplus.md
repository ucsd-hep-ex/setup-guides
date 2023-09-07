# CERN Lxplus

## Work directory

As of ~2022, CERN recommends using your `eos` directory for all work. Make a CERNBox account to get an `eos` directory: https://swan.docs.cern.ch/intro/cernbox/.

It should then show up at `/eos/user/<first letter of your username>/<username>`. You can then install conda / mamba, CMSSW releases, repositories etc. in this directory.


## Persistent screen / tmux

See https://hsf-training.github.io/analysis-essentials/shell-extras/README.html and, in particular https://hsf-training.github.io/analysis-essentials/shell-extras/persistent-screen.html. 

But note that their method to get a keytab is outdated! This is the current recommendation:

```bash
cern-get-keytab --keytab private/<username>.kt --user --login <username>
```

**TODO:** Update once https://github.com/hsf-training/analysis-essentials/pull/66 gets merged.