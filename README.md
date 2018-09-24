# Minecolonies Schematics Repository

Contains all schematics that anyone can use in Minecolonies Mod.
Used by structurize

### Adding new style
If you wish to have your style available directly in our mod, create a PR with adding your name to `branches.json`
We will create you a new branch just for you, if we will consider you being able to have it - Patreons, widely accepted by the community on our forum etc.

### Updating your style
Just create a PR with updated files, we will try to merge it asap. The game automatically checks for new updates

### Structure 
folders: `(branch root)/{styles}/{heads}/{types}/{files}`<br>
_if you don't want to show any of style/head/type just unlist them from their respective lists_

`branches.json`
- branches - list of all branches, only in the master branch

`styles.json`
- styles - list of all your styles (== `{style name}`), in other branches (not the master one)
- author - author's name

`{style name}/style.json` 
- name/description/image (optional)/joke (optional) - information about your style
- base (optional) - base style
- default (optional, only can be `true`) - if default is present then it will be downloaded automatically on the first startup
- registry (compulsory only if default is present) - a list of heads that each style should have otherwise any missing head will be filled from lower level (style > base > default), registry can be a list or a reference to heads (`$heads`)
- heads - list of sub folders (== `{head name}`)

- `{head name}` (for each head in heads), can be replaced by `any` to match every head from heads
  - types - list of types (== `{type name}`)
  - registry (compulsory only if default is present) - same functionality as above, registry can be a list or a reference to types (`$types`)
  
  - `{type name}` (for each type in types), can be replaced by `any` to match every type from types
    - files - list of files
    - registry (compulsory only if default is present) - same functionality as above, registry can be a list or a reference to types (`$files`)

##### Website:
https://www.minecolonies.com/
