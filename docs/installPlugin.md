## How to Install Vim Plugins Without a Plugin Manager

### 1. Create or find the .vim directory
Usually, we will have a `.vim` directory in our home folder. This is where we
should put plugins and syntax files for vim. This is just a convention, however,
so feel free to put them wherever you want.

### 2. Create a 'bundle' directory inside the .vim folder
This is another convention.

### 3. Copy your plugin to this directory
If its just a single file with a `.vim` filetype, create a directory here and put
the file inside, else copy the plugin directory here. For `nerdtree` it will
look like below:
```sh
bundle
└── nerdtree
    ├── CHANGELOG
    ├── LICENCE
    ├── README.markdown
    ├── autoload
    │   ├── nerdtree
    │   │   └── ui_glue.vim
    │   └── nerdtree.vim
    ├── doc
    │   ├── NERD_tree.txt
    │   └── tags
    ├── lib
    │   └── nerdtree
    │       ├── bookmark.vim
    │       ├── creator.vim
    │       ├── event.vim
    │       ├── flag_set.vim
    │       ├── key_map.vim
    │       ├── menu_controller.vim
    │       ├── menu_item.vim
    │       ├── nerdtree.vim
    │       ├── notifier.vim
    │       ├── opener.vim
    │       ├── path.vim
    │       ├── tree_dir_node.vim
    │       ├── tree_file_node.vim
    │       └── ui.vim
    ├── nerdtree_plugin
    │   ├── exec_menuitem.vim
    │   └── fs_menu.vim
    ├── plugin
    │   └── NERD_tree.vim
    └── syntax
        └── nerdtree.vim
```

### 4. Set your vim runtimepath
Now that our plugin is where we want it, we need to tell vim where to find it
every time we start it up. Our runtimepath is where vim looks for scripts,
syntax files, plugins and other things to include in our vim environment.
Inside vim, we can find our runtimepath with the following command:
```sh
set runtimepath?
```

To update our runtimepath and load our new plugin, we're going to edit our .vimrc
which should be located in our home folder. The syntax to add a directory to our
runtime path looks like this:
```sh
set runtimepath^=~/.vim/bundle/ctrlp.vim
```

### 5. Reload the vimrc
We can call the following command:
```sh
source ~/.vimrc
```
or just close and restart vim.

### References
[Copied and pasted from here](https://howchoo.com/g/ztmyntqzntm/how-to-install-vim-plugins-without-a-plugin-manager)
