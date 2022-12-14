Autosave editor for [Slay the Spire](https://store.steampowered.com/app/646570/Slay_the_Spire/).

The code has been written as modular as possible for easy customization.

Use with caution, as it can really ruin the fun. But for me, sometimes I prefer to extract all the fun as fast as possible and then begone with my life.

## How the script works
- It starts by finding an autosave file, usually named with this format: `<Name of the character>.autosave`, for example `DEFECT.autosave`
- It will then try to decrypt the save data and convert it to a JSON editable format
- You can then edit the save file as you want
- Then rewrite it back to the autosave file 

## How to
- Install python3 
- Inside `main.py`, Change the `save_file_path` according to your game installation so that it points to the *root path* of the autosave file. 
  - By default it will be inside the default steam folder `..../Steam/steamapps/common/SlayTheSpire/saves`
  - I used Linux, so if you use Windows you will need to change the path and make sure it is absolute path
- Edit the `main.py` as you need. You can change your health, build your own deck, etc
- Go inside the game, pick your prefered character, then on the first encounter, choose `Save & Quit`
- From the main menu (no need to close the game), just run `main.py` with the command `python3 main.py`
  - On each script run, the script will dump the save data BEFORE the modification and save it inside `backups` folder. Just in case you messed up something, you can edit back according to it
- After that, click `Continue`, and enjoy!

## Note

Currently, there are only configuration for The Defect. But actually if you can already see the save data in JSON you can basically change anything you want, so feel free to modify the code and add your own preference!

It is really just a basic JSON edit.

## Disclaimer

I got the save file encryption logic from [Kirill89's gist](https://gist.github.com/Kirill89/514edad0ac80af7dfc036871ccf0f877) written in JS. What I did was only re-write it in python and added some feature so that the save data can be programmatically edited.
