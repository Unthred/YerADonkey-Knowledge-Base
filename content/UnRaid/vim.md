/*
Title: Vim Syntax Highlighting
Description: Howe to get and speed up vim's syntax hightlighting
Sort: 0
*/

1. Turn on vim in the Nerd Pack
2. mkdir ~/.vim
3. Download ```` wget -O ~/.vim/yaml.vim http://www.vim.org/scripts/download_script.php?src_id=2249````
4. Add 
````au BufNewFile,BufRead *.yaml,*.yml so ~/yaml.vim```` 
 to ~/.vimrc
