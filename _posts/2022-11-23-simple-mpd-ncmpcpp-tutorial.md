---
layout: post
title: Simple mpd+ncmpcpp setup tutorial
date: 2022-11-23
---

### Disclaimer:
This tutorial does not cover any advanced features
of mpd including streaming over a network. This is to help set up a local instance of mpd for a single user.

### Assumptions:

- Your distro's default repository ships with both mpd and ncmpcpp.
(or you are able/willing to compile from source)

- Your current audio server is Pipewire (run `pactl info` to confirm)

- You're using SystemD as your init system

### References:
- [My mpd.conf](https://github.com/basedghost/dotfiles/blob/main/.config/mpd/mpd.conf)

- For [more documentation on how to use mpd](https://mpd.readthedocs.io/en/latest/user.html)

- For [more information on ncmpcpp](https://rybczak.net/ncmpcpp/)

# Install required packages:

First you'll need to install both mpd and ncmpcpp with your distros main package manager.
Since I am on Arch Linux, I just have to run:

`sudo pacman -S mpd ncmpcpp`

If for some reason they're unavailable, you may have to compile them manually.
Additionally, you can install `mpc` to control mpd via command-line.

ex: `mpc volume -2`, `mpc random on`, etc.

This is useful for mapping mpd controls to keybindings.

# Configure mpd

Now that mpd is installed, you'll want to configure it.
The system-wide config file for mpd can be found in /etc/mpd.conf.
Since we'll be running it as a user daemon, the config file
must reside in your home directory. (specifically ~/.config/mpd/mpd.conf)
First, make a directory for the mpd config:

`mkdir ~/.config/mpd/`

Then copy the config file over.

`sudo cp /etc/mpd.conf ~/.config/mpd/mpd.conf`

Now open that file in your favorite text editor
(for simplicity sake I'm using nano in this example):

`nano ~/.config/mpd/mpd.conf`

Make sure your music and playlist directories are set correctly.
```
music_directory    "~/Music"
playlist_directory "~/mpd-playlists"
```
The next thing you'll want to do is find the list of audio outputs in the config and add the following:
```
audio_output {
    type         "pipewire"
    name         "Pipewire Multimedia Service"
}
```
This creates an audio output for pipewire. Feel free to name it whatever you'd like.

![image](https://user-images.githubusercontent.com/91919356/203658949-84a7cbad-541d-4044-bddb-50ae78267a7d.png)

ncmpcpp has this really neat music visualizer feature.
For that, you'll need to add this as an output:
```
audio_output {
    type                    "fifo"
    name                    "Visualizer"
    path                    "/tmp/mpd.fifo"
    format                  "44100:16:2"
}
```
That should be it for configuring mpd.
Now to start it!

# Starting/stopping mpd

You can start mpd (as a user daemon) with the following command:

`systemctl --user start mpd`

If you'd like mpd to autostart at login:

`systemctl --user enable mpd`

If you'd like to stop mpd:

`systemctl --user stop mpd`

Once mpd is started, open a terminal and run:
`ncmpcpp`

Voila! You now have mpd running with ncmpcpp as a front-end for it.
To show the keybindings for ncmpcpp, press F1.

This may be a simple tutorial, but I hope it can prove to be useful!

-H
