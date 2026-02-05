# My Vim Dotfile

A minimalistic Vim configuration with custom plugin management - no bloated plugin managers needed.

## Features

- **🚀 Lightweight & Fast** - Minimal configuration for maximum performance
- **🔧 Custom Plugin Management** - Simple, transparent plugin system built from scratch
- **📦 Easy Plugin Addition** - Add any Vim plugin by just adding one line
- **⚡ Auto-Installation** - Plugins automatically clone on Vim restart
- **🎨 Clean & Organized** - Modular structure for easy customization
- **🔑 Flexible Keybindings** - Easy to configure custom keybindings for each plugin

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/AnubhabMukherjee2003/my-vim-dotfile.git ~/.vim
```

### 2. Configure Your .vimrc

Point your `.vimrc` file to source the configuration:

```bash
echo "source ~/.vim/vimrc" > ~/.vimrc
```

Or if you already have a `.vimrc`, add this line:

```vim
source ~/.vim/vimrc
```

### 3. Start Vim

```bash
vim
```

That's it! Your Vim is now configured and ready to use.

## Adding New Plugins

### Step 1: Add Plugin to plugins.vim

Edit `~/.vim/plugins.vim` and add a line for your plugin:

```vim
" Example format
call InstallPlugin('author/plugin-name')
```

### Step 2: Restart Vim

The plugin will automatically clone on restart.

### Step 3: Configure (Optional)

Add keybindings or styling in your configuration:

```vim
" Example: Adding keybinding for vim-commentary
vnoremap <leader>c :Commentary<CR>

" Example: Configuring plugin colors
let g:plugin_color_scheme = 'dark'
```

### Real-World Examples

```vim
" In ~/.vim/plugins.vim
call InstallPlugin('tpope/vim-commentary')
call InstallPlugin('tpope/vim-surround')
call InstallPlugin('preservim/nerdtree')

" Then add keybindings in your config (ex: keybindings.vim)
nnoremap <C-n> :NERDTreeToggle<CR>
vnoremap <leader>c :Commentary<CR>
```

## Customization

### Adding Keybindings

Edit `~/.vim/keybindings.vim` or create a separate keybindings file:

```vim
" Example keybindings
nnoremap <leader>n :NERDTreeToggle<CR>
nnoremap <leader>f :Files<CR>
vnoremap <leader>c :Commentary<CR>
```

### Styling Plugins

Configure plugin appearance in your vimrc:

```vim
" Example styling
let g:NERDTreeWinSize = 30
let g:airline_theme = 'minimalist'
```

## Why This Approach?

- **Simplicity** - Just add one line to install a plugin
- **Automatic** - No manual cloning or Git commands needed
- **Control** - You know exactly what's installed
- **Fast** - Minimal overhead, uses Vim's native features
- **Transparent** - Easy to see what plugins are declared
- **Self-contained** - Everything in one dotfile repository

## Contributing

Feel free to fork this repository and customize it to your needs. If you have suggestions or improvements, pull requests are welcome!

## License

Free to use and modify as you wish.

---

**Happy Vimming! 🎉**
