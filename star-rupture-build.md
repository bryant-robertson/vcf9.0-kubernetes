# Update Ubuntu

```
sudo apt update && sudo apt full-upgrade -y && sudo apt autoremove -y
```

# Install Wine & Deps

```
sudo apt install -y wine winetricks xvfb lib32z1  # Core Wine + headless X
winetricks vcrun2019 corefonts  # Windows DLLs (run as steam user later if needed)
```

# Install steamCMD using apt

```
# Enable 32-bit architecture (required even on 64-bit system)
sudo dpkg --add-architecture i386

# Make sure multiverse is enabled (usually already is on 24.04 server/desktop)
sudo add-apt-repository multiverse -y

# Update package lists
sudo apt update

# Install SteamCMD + required 32-bit libraries
sudo apt install steamcmd lib32gcc-s1 -y
```

# Verify it worked

```
steamcmd +quit
```

# Create a directory for your game server

```
mkdir -p ~/games/star-rupture
```

# notes
This game needs wine and a few things that are a pain in the ass to install and get working. I used grok to get through it.

