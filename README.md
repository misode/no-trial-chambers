# Update 1.21 without trial chambers
Enables the Update 1.21 experimental features, but disables the trial chambers and breeze.

[![modrinth](https://cdn.jsdelivr.net/npm/@intergrav/devins-badges@3/assets/cozy/available/modrinth_vector.svg)](https://modrinth.com/datapack/no-trial-chambers) [![download](https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/badges/download-the-data-pack.svg)](https://github.com/misode/no-trial-chambers/releases)

<table>
  <thead>
    <th>Enabled</th>
    <th>Disabled</th>
  </thead>
  <tbody>
    <td>
      <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/BlockSprite_crafter.png"> Crafter
      <br>
      <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/BlockSprite_copper-bulb.png"> <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/BlockSprite_lit-copper-bulb.png"> Copper bulb
      <br>
      <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/BlockSprite_chiseled-copper.png"> <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/BlockSprite_copper-grate.png"> Copper blocks
      <br>
      <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/BlockSprite_chiseled-tuff.png"> <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/BlockSprite_polished-tuff.png"> <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/BlockSprite_tuff-bricks.png"> Tuff blocks
    </td>
    <td>
      <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/EnvSprite_trial-chambers.png"> Trial chambers
      <br>
      <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/BlockSprite_trial-spawner.png"> <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/BlockSprite_vault.png"> Trial spawner and vault
      <br>
      <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/BlockSprite_heavy-core.png"> Heavy core
      <br>
      <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/EntitySprite_breeze.png"> Breeze
      <br>
      <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/EntitySprite_bogged.png"> Bogged
      <br>
      <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/ItemSprite_trial-key.png"> Trial key
      <br>
      <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/ItemSprite_wind-charge.png"> Wind charge
      <br>
      <img src="https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/sprites/ItemSprite_ominous-bottle.png"> Ominous bottle
    </td>
  </tbody>
</table>

## Data pack instructions

**After installation, DON'T enable the separate "update_1_21 (feature)" data pack!**

<details><summary>Adding to a new singleplayer world</summary>

1. Open the "Data Packs" selection screen when creating a new world  
![](https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/new_world_screen.png)
2. Drag the downloaded datapack zip file onto the game window
3. Move data pack to the "Selected" column and click "Done"  
![](https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/select_data_packs.png)
4. Accept the "Experimental Features Warning"  
![](https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/experimental_features_warning.png)
5. Change any other world settings and click "Create New World"  
![](https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/create_new_world.png)

</details>

<details><summary>Adding to an existing singleplayer world</summary>

1. Select your world and click "Edit"  
![](https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/edit_world.png)
2. Click "Open World Folder"  
![](https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/open_world_folder.png)
3. Enable the "Update 1.21" feature flag `level.dat`. A simple way to do this is by installing the [NBT Viewer](https://marketplace.visualstudio.com/items?itemName=Misodee.vscode-nbt) extension for [VSCode](https://code.visualstudio.com/)  
![](https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/nbt_viewer_install.png)
4. Open the `level.dat` file in VSCode by dragging the file from the file explorer to the VSCode window
5. Inside `Data`, add a new list tag called `enabled_features`  
![](https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/nbt_enabled_features.png)
6. Inside this list, add two new string tags with `minecraft:vanilla` and `minecraft:update_1_21`. Select the yellow string icon when adding the first tag.  
![](https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/nbt_update_1_21.png)
7. Press `Ctrl + S` to save the file, make sure the world is not open in-game when editing the file!
8. In the world save folder, find the `datapacks` folder and put the downloaded zip file in there  
![](https://raw.githubusercontent.com/misode/no-trial-chambers/main/images/existing_world_datapack.png)
9. You can now open the world!

</details>

<details><summary>Adding to a new multiplayer server</summary>

1. Download the server jar from the bottom of the [1.20.4 article](https://www.minecraft.net/en-us/article/minecraft-java-edition-1-20-4)
2. Place the `server.jar` file in the server folder
3. Inside this same folder, create the folders `world/datapacks/`
4. Put the downloaded zip file in there
5. Run the server jar for the first time
```sh
java -Xmx1024M -Xms1024M -jar server.jar nogui
```
6. Agree to the EULA by editing `eula.txt`
7. Run the server jar again. You should see `Found new data pack file/update_1_21_no_trial_chambers_1.20.4.zip, loading it automatically` in the log.

</details>

<details><summary>Adding to an existing multiplayer server</summary>

1. Shut down the server
2. Modify the `world/level.dat` file following the same instructions from "Adding to an existing singleplayer world"
3. Add the downloaded zip file to the `world/datapacks/` folder
4. Restart the server

</details>
