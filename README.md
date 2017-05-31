# Electron
Electron Template to build and release Monogatari games, this template makes use of [Electron Builder](https://github.com/electron-userland/electron-builder), a package made to make the distribution of electron apps easier. As such, this project uses a 2 directory structure, the root directory is relevant to electron builder, it contains a package.json file stating information and settings for your game as well as the build directory where the icon for the game is stored.

## What will you need?

* NodeJS installed (Latest version)
* A game made in Monogatari

## Step One: Fill the Root `package.json` file

The `package.json` file is really important since it holds the information to build your game, the properties you want to change are:

`name`: Your game's name, lowercased and must not contain spaces.

`productName`: Your game's name, this is the name that will be displayed

`version`: Your game's version, versioning is really important and if you need help, here's a nice guide to it: http://semver.org/

`description`: Your game's description

`author`: Your name and email in the following format: `"Your Name <example@example.com>"`

`license`: The license under which your game is released, this is also very important!

`appId`: The id with which your game will be identified, it follows the following structure: `com.example.mygame`.

`executableName`: Same as `productName`

`synopsis`: Same as `description`


## Step Two: Add your icons to the build directory

Two icons must be added, one for Widnows and one for macOS. The Linux icon will be derived from this two.

The Windows icon must be a ico file named `icon.ico`

The macOS icon must be a icns file named `icon.icns`

If you don't know how to create this file formats, here's a nice web utility that will do it for you: https://iconverticons.com/online/

## Step Three: Copy your game files to the app directory

Yes, as simple as that, just copy all yopur game's files to the app directory.

## Step Four: Test your game

On macOS and Linux, this is really simple, just pop open a terminal window, navigate to the electron template root directory where the first package.json file is and then type the following:

`npm install`

That will have installed all the needed packages.

`npm run start`

Your game should start now and you can test it.

## Step Five: Build Your game and Distribute it!

Once you've made sure everything is ok, you are ready to build the distributable files, againg, this is very simple and only needs you to type:

`npm run dist`

It can take a while downloading other needed things and building the packages but after it finishes, you should be able to see all your packages inside the `dist` directory ready to be shipped.
