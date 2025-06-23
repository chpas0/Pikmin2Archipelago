# Pikmin 2 Archipelago Setup Guide
## Required Software
- Dolphin Emulator: https://dolphin-emu.org/download/
- Archipelago: https://github.com/ArchipelagoMW/Archipelago/releases
- Pikmin 2 APWorld: https://github.com/chpas0/Pikmin2Archipelago/releases
- A Pikmin 2 USA .iso file
## Installing the APWorld
Put the pikmin2.apworld file in the ```custom_worlds``` folder of your Archipelago installation. You can also just double-click the file to automatically install it.
## Configuring the YAML file
### What is a YAML file and why do I need one?
Your YAML file contains a set of configuration options which provide the generator with information about how it should generate your game. Each player of a multiworld will provide their own YAML file. This setup allows each player to enjoy an experience customized for their taste, and different players in the same multiworld can all have different options.
### Where do I get a YAML file?
Once you've installed the apworld, you can generate a yaml using the ```Generate Template Options``` button in the ArchipelagoLauncher. It can be found in ```Players/Templates``` after you have done so. The name of the file will be ```Pikmin 2.yaml```.

If the .yaml file is missing in your ```Players/Templates``` folder, then please go through the apworld installation steps again, and double check that everything was done correctly.

**IMPORTANT NOTE: The .yaml file has multiple options under ```Item & Location Options```, these are all untested and may not work as intended.**

## Generating a Multiworld Game
### Step 1
Place all of the players' ```.yaml``` files into the ```Players``` folder of your Archipelago installation (NOT the ```Players/Templates``` folder).
### Step 2
Open the Archipelago Launcher (```ArchipelagoLauncher.exe```) and click the "Generate Button". If the generation succeeds, this should create a ```.zip``` archive in the ```output``` directory of your Archipelago installation.
### Step 3
Unzip the archive that was just generated. There should be a ```.json``` file inside called ```pikmin2_<seed>_<player_name>```. This file will be referred to as the Pikmin 2 setup file for the rest of the guide.
### Step 4
Run the ```patcher.exe``` executable that was included with the Pikmin 2 APWorld release. It will prompt you for the Pikmin 2 setup file (the ```.json``` file from Step 3) and the Pikmin 2 USA .iso file. It will output a patched version of the game to the same directory that the executable is in, called ```pikmin2_<seed>.iso```.
### Step 5
Re-open the Archipelago Launcher, and click the ```Pikmin2Client``` button. You will be prompted for the patched Pikmin 2 .iso file and the Pikmin 2 setup file. If this is your first time running the client, you will also be asked for your Dolphin executable file and your Dolphin save directory (usually ```C:/Users/<username>/AppData/Roaming/Dolphin Emulator/GC/USA/Card A```); these paths will be saved to your ```host.yaml``` so you don't need to select them each time.
### Step 6
The client and an instance of Dolphin should launch. You can then connect to the Archipelago server!

**IMPORTANT NOTE: If either the client or the Dolphin instance are closed, you must close the other one. Items obtained while the client is closed will be lost!**

## Hosting a Multiworld Game
You can upload the generated ```.zip``` file (here)[https://archipelago.gg/uploads] to launch a server.

**IMPORTANT NOTE: You must delete the ```.json``` file (setup file) from the .zip archive before uploading it, otherwise the server will not launch.**