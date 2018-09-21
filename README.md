# Minecolonies Schematics Repository

Contains all schematics that anyone can use in Minecolonies Mod.
Used by structurize

### Adding new style
If you wish to have your style available directly in our mod, create a PR with adding your name to branches.json
We will create you a new branch just for you, if we will consider you as being able to have it - Patreons, accepted by community on our forum etc.

### Updating your style
Just create a PR with updated files, we will try to merge it asap. The game automatically checks for new updates

### Structure 
folders: `(branch root)/{styles}/{heads}/{types}/`<br>
_if you don't want to show any of style/head/type just unlist them from their respective lists_

`branches.json`
- branches - list of all branches (== `{branch name}`), only in the master branch (aka default branch)

`{branch name}.json`
- styles - list of all your styles (== `{style name}`)
- author - author's name

`{style name}/{style name}.json` 
- heads - list of sub folders (== `{head name}`)
- name/description/image (optional)/joke (optional) - information about your style
- base (optional) - base style
- default (optional) - if default is present (with `true`) then it will be downloaded automatically on the first startup
- registry (optional) - a list of heads that each style should have otherwise any missing schematic will be filled from lower level (style > base > default), registry can be a list or a reference to heads (`$heads`)

`{style name}/{head name}/{head name}.json`
- types - list of types (== `{type name}`)
- registry (optional) - same functionality as above, registry can be a list or a reference to types (`$types`)

`{style name}/{head name}/{type name}/{type name}.json`
- files (optional) - list of files
- registry (optional) - same functionality as above, registry can be a list or a reference to types (`$files`)

##### Website:
https://www.minecolonies.com/
