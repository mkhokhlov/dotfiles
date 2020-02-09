" ====== Vundle stuff ======
set nocompatible              " be iMproved, required
filetype off                  " required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

" let Vundle manage Vundle, required
Plugin 'VundleVim/Vundle.vim'
Plugin 'altercation/vim-colors-solarized'
Plugin 'tpope/vim-sensible'
Plugin 'tpope/vim-surround'
Plugin 'tpope/vim-unimpaired'

" ====== vim-codemt stuff ======
" Add maktaba and codefmt to the runtimepath.
" (The latter must be installed before it can be used.)
Plugin 'google/vim-maktaba'
Plugin 'google/vim-codefmt'
" Also add Glaive, which is used to configure codefmt's maktaba flags. See
" `:help :Glaive` for usage.
Plugin 'google/vim-glaive'
" ====== END OF vim-codemt stuff ======

" All of your Plugins must be added before the following line
call vundle#end()            " required
filetype plugin indent on    " required
" To ignore plugin indent changes, instead use:
"filetype plugin on
" ====== END OF Vundle stuff ======

" ====== vim-codemt stuff ======
" the glaive#Install() should go after the "call vundle#end()"
call glaive#Install()
" Optional: Enable codefmt's default mappings on the <Leader>= prefix.
Glaive codefmt plugin[mappings]
" let g:java_format_jar_command="java -jar " . $HOME . "/bin/google-java-format-1.7-all-deps.jar"
" Glaive codefmt google_java_executable=`g:java_format_jar_command`
Glaive codefmt google_java_executable="java -jar "
Glaive codefmt google_java_executable+=`$HOME`
Glaive codefmt google_java_executable+="/bin/google-java-format-1.7-all-deps.jar"
" ====== END OF vim-codemt stuff ======

" vim-color-solarized
syntax enable
set background=dark
colorscheme solarized

" Powerline requires vim compiled with +python option.
" sudo apt install vim-nox
" pip show powerline-status | grep Location # Get the prefix for the path below.
set rtp+=$HOME/.local/lib/python2.7/site-packages/powerline/bindings/vim

" my random preferences
set expandtab
set shiftwidth=2
set tabstop=2
set hidden
set nu
set cursorline
set ttimeoutlen=100
map <F2> :ls<CR>:b<Space>
nnoremap <F3> :m .+1<CR>==
nnoremap <F4> :m .-2<CR>==
inoremap <F3> <Esc>:m .+1<CR>==gi
inoremap <F4> <Esc>:m .-2<CR>==gi
vnoremap <F3> :m '>+1<CR>gv=gv
vnoremap <F4> :m '<-2<CR>gv=gv

