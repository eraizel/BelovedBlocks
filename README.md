# BelovedBlocks

Development builds available for each commit [on our Jenkins server](http://jenkins.carrade.eu/job/BelovedBlocks/).

This plugin is [available on BukkitDev](http://dev.bukkit.org/bukkit-plugins/beloved-blocks/).  
Please note, this README reflects the last development version. Some features listed here may not be in the version published on BukkitDev.

This plugin was made by Amaury Carrade and Florian Cassayre; it is currently translated in English, French and German.


1. [Features](#features)
   1. [New items](#items)
   2. [Stonecutter](#stonecutter)
   3. [Saw](#saw)
1. [Commands & permissions](#commands--permissions)
   1. [Commands](#commands)
   2. [Permissions](#permissions)
1. [Configuration](#configuration)
1. [License](#license)


## Features

The 1.8 version of minecraft has removed the items that corresponds to some unobtainables blocks in survival. Although their corresponding items doesn't exist anymore, the blocks still exist. You can place them by doing a  `/setblock` command with some metadata arguments.

This plugin instances new items that transforms themselves into the desired special block when placed by a player.

![](http://amaury.carrade.eu/files/Minecraft/Plugins/BelovedBlocks/BB_Banner.png)

*Some of the seamless blocks featured by the plugin*

### Items

Each seamless block is represented by a similar item with a glowing enchantment effect (that can be disabled for each block in the [configuration](#configuration)). They also have a custom name (also configurable). The crafts are the same for the three blocks:

![](http://amaury.carrade.eu/files/Minecraft/Plugins/BelovedBlocks/BB_Crafts_Stones.gif)

The smooth log blocks can also be crafted using the same process, except with wooden logs:

![](http://amaury.carrade.eu/files/Minecraft/Plugins/BelovedBlocks/BB_Crafts_Logs.gif)

Those crafts can be disabled.

All those items can be salvaged to get the materials back ; simply place an item in a crafting grid.

### Stonecutter

The stonecutter is a tool that can smooth any of the three double slabs blocks. To use it, simply right click with this tool on the wished block and it will permute to a smooth block. Each use will decrease the item's durability by 1. The unbreaking enchantment does work when applied. The stonecutter can be crafted like shears in exceptions that the iron is replaced by diamonds:

![](http://amaury.carrade.eu/files/Minecraft/Plugins/BelovedBlocks/BB_Crafts_Stonecutter.png)


The craft can be disabled.

The basic double slabs block → the seamless version of this block:

![](http://amaury.carrade.eu/files/Minecraft/Plugins/BelovedBlocks/BB_Stones_DoubleSlabs_Transformations.png)

The process can be reverted (use the tool on a smooth block to turn it back into the original block).

### Saw

The saw is a tool that can move the bark around any of the six log blocks. To use it, simply right click with this tool on the wished log block to move the bark. The bark can have 4 different positions (tree of them follows, the tree axes and one has bark all around the texture). Each use will decrease the item's durability by 1. The unbreaking enchantment does work when applied. The saw can be crafted like this (the symmetric craft also works):

![](http://amaury.carrade.eu/files/Minecraft/Plugins/BelovedBlocks/BB_Crafts_Saw.png)

The craft can be disabled.

Note: when breaking blocks with the saw, it has a small chance to break. This percentage can be modified in the configuration.

## Commands & permissions

### Commands

A few commands allow you to get the tools and blocks added by this plugin.

The main command is `/belovedblocks`, or `/bb` (an alias).

 * `/bb give tool <stonecutter|saw> [receiver]`: gives the needed tool to you, or to the receiver.
 * `/bb give block <name> [amount] [receiver]`: gives the blocks of BelovedBlocks to you (or to the receiver), where `name` is one of the following:
   * `stone`, `sandstone`, `red-sandstone`, `quartz`;
   * `oak`, `spruce`, `birch`, `jungle`, `acacia`, `dark-oak`.

Tip: use autocompletion.


### Permissions

The permissions tree is the following one:

 * `belovedblocks.give`
    * `tools`
       * `stonecutter`
          * `self`
          * `other`
       * `saw`
          * `self`
          * `other`
    * `blocks`
       * `stone`
          * `self`
          * `other`
       * `sandstone`
          * `self`
          * `other`
       * `red-sandstone`
          * `self`
          * `other`
       * `quartz`
          * `self`
          * `other`
       * `oak`
          * `self`
          * `other`
       * `spruce`
          * `self`
          * `other`
       * `birch`
          * `self`
          * `other`
       * `jungle`
          * `self`
          * `other`
       * `acacia`
          * `self`
          * `other`
       * `dark-oak`
          * `self`
          * `other`

As example:
 * to allow someone to give to himself only some smooth red sandstone, use the permission `belovedblocks.give.blocks.red-sandstone.self`;
 * to allow someone to give any block to anyone, use `belovedblocks.give.blocks`.


## Configuration

The plugin can be configured using the `config.yml` file (it can be found at `/plugins/BelovedBlocks/config.yml` in your server's folder or [here on GitHub](https://github.com/AmauryCarrade/BelovedBlocks/blob/master/src/main/resources/config.yml)).

## License

GPLv3. See `LICENSE` file for more details.
