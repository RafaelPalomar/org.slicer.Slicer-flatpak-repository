# Slicer Flatpak (Alpha) :warning: :construction:

:warning: Please note that this Flatpak distribution of Slicer is in **ALPHA STAGE**. This means that it is still in development, and you should expect limited functionality and potential bugs. :warning:

## Installing Flatpak

First, you need to install Flatpak on your system. The instructions for doing this will vary depending on your distribution. Here are examples for Debian/Ubuntu and Arch Linux:

### Debian/Ubuntu

You can install Flatpak on Debian/Ubuntu with the following command:

```bash
sudo apt install flatpak
```

### Arch Linux

On Arch Linux, you can use pacman to install Flatpak:

```bash
sudo pacman -S flatpak
```

For other distributions, check out the [official Flatpak setup guide](https://flatpak.org/setup/).

## Adding the Flathub repository

The Slicer Flatpak depends on some runtimes that are hosted on Flathub. If you haven't already added the Flathub repository, you can do so with the following command:

```bash
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

This command will add the Flathub repository as a remote, which will allow you to install necessary runtimes.

## Adding this Flatpak repository

To use the Flatpak version of Slicer, you first need to add this repository to your list of remotes. You can do this by running the following command in your terminal:

```bash
flatpak remote-add --if-not-exists Slicer https://github.com/RafaelPalomar/org.slicer.Slicer-flatpak-repository/raw/main/slicer.flatpakrepo
```

This command will add this repository as a remote named `Slicer`.

## Installing Slicer

Once both repositories have been added, you can install Slicer by running:

```bash
flatpak install Slicer org.slicer.Slicer
```
