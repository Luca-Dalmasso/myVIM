# myVIM
My configuration for VIM CLI editor.

## content
-   directory setup
-   vimrc configuration file setup
-   adding plugins and the maokai colorstheme to Vim
-   what to expect
-   useful links

### directory setup
First you need to have the following directory structure in your `home`: <br>
```
~.vim/
 ├── autoload/
 ├── backup/
 ├── colors/
 └── plugged/

 ```
To do this, type the command below:

    mkdir -p ~/.vim ~/.vim/autoload ~/.vim/backup ~/.vim/colors ~/.vim/plugged

### vimrc configuration file setup

Configuring your `.vimrc` file lets you use the full power of Vim. It's a configuartion file that allow to customize the Vim Editor with commands and plugins.<br>
The `vimrc` file must be present in your `~` (home) directory to be automatically loaded by Vim.

If not yet done, clone this repo in your home folder using the command below:

    git clone git@github.com:Luca-Dalmasso/myVIM.git ~ && cd myVIM

Copy the `.vimrc` file in your `~` (home) directory:

    cp -f .vimrc ~

### adding plugins and the maokai colorstheme to Vim
The Vim plugins are used to enhance the Vim Editor functionalities.<br>
To easily add plugins into Vim, the `vim-plug` plugin manager is used.<br>
To install the vim-plug plugin, run this command:

    curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim

In the included `.vimrc` there are already 2 plugins included:
-   Asynchronous Lint Engine (ALE).
-   NERDTree

If you want too check where are the plugins included in the `.vimrc` you should be able to find the following lines inside it:
```
" PLUGINS ---------------------------------------------------------------- {{{

call plug#begin('~/.vim/plugged')


  Plug 'dense-analysis/ale'

  Plug 'preservim/nerdtree'


call plug#end()

" }}}

```

You can add other plugins by adding the `'Plug <plug_name>'` in between the two `call plug#` lines like above.

Plugins are not yet ready to be used, the must be downloaded and installed by the plugin manager.

To do so, open vim and type `:PlugInstall`.

You can easily add color schemes to Vim to change the default colors. Do a search for Vim color schemes and you will find many, many choices.

Installing a color scheme is a simple as adding a `<colorscheme>.vim` file to the `~/.vim/colors/` directory and the use the wanted colorscheme by adding it in the `.vimrc` file with the command `colorscheme <colorscheme>`. The colorscheme declared in the .vimrc file is the `molokai` and in order to be used it must be donwloaded and installed with the commands below:

    cd ~/.vim/colors

    curl -o molokai.vim https://raw.githubusercontent.com/tomasr/molokai/master/colors/molokai.vim

### what to expect

This is how Vim looks like **without** this configuration:
![before](./img/a.png)
This is how Vim looks like **with** using this configuration:
![before](./img/b.png)

Note:<br>
The directory tree showed on the left is not present by default, it can be opened/closed by pressing the `TAB` key. This feature is not present by default on the Vim editor, it has included by the `NERDTree` plugins.

Extended documentation of the two plugins included can be found in the links below:

    https://github.com/dense-analysis/ale


    https://github.com/preservim/nerdtree


## useful resources

**Vim cheatsheet**

    https://vimsheet.com

**Vim webpage**

    https://www.vim.org

**References**

    https://www.freecodecamp.org/news/vimrc-configuration-guide-customize-your-vim-editor/

