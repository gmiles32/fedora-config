# Fedora Configuration

I was inspired by NixOS so come up with a way to maintain a general configuration for Fedora. This ansible playbook is meant to be run on a local machine, and will install the packages that I use, enable non-free repositories, and install all gtk themes that I like. In the future, I am trying to configure it so that gnome extensions will be installed, and so that the themes are set by the playbook, rather than just being installed. I also want to set fonts via commandline.

## Running the playbook

```bash
just # this will load all the dependencies
just configure host all # this will run through the playbook for the specific host, can use `local host`
```

## After running

Right now, to install all the gnome extensions using [gnome-extension-cli](https://github.com/essembeh/gnome-extensions-cli), use the following command:
```bash
gext --filesystem install user-theme@gnome-shell-extensions.gcampax.github.com blur-my-shell@aunetx rounded-window-corners@yilozt caffeine@patapon.info drive-menu@gnome-shell-extensions.gcampax.github.com
```

I have to restart in order for extensions to work.

For fonts I have been using `Roboto 11` and `JetBrains Mono 11`.

I've also been using dynamic wallpapers from [here](https://github.com/manishprivet/dynamic-gnome-wallpapers)

