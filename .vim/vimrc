" http://blog.adamlowe.com/2009/12/vim-destroys-all-other-rails-editors.html
" start
filetype off

call pathogen#infect()

filetype plugin indent on
set tabstop=4
set shiftwidth=4
set softtabstop=4
set autoindent
set noexpandtab
" end

" Solarized
" start
syntax enable
set background=dark
colorscheme solarized
call togglebg#map("<F5>")
" end

" http://damien.lespiau.name/blog/2009/03/18/per-project-vimrc/
" start
" set exrc    " enable per-directory .vimrc files
" set secure  " disable unsafe commands in local .vimrc files
" end

" my stuff
set fileencodings=utf-8
set hlsearch
set backupdir=/tmp
set directory=/tmp
set ignorecase
set smartcase
set ruler
set guifont=Consolas:h12
" end

"-- Show whitespace chars
set listchars=tab:?\ ,trail:?,extends:>,precedes:<
set list

"-- Remove trailing whitespaces from lines
autocmd FileType php autocmd BufWritePre <buffer> :call setline(1,map(getline(1,"$"),'substitute(v:val,"\s\+$","","")'))

"-- Press F5 to Clean Current Buffer
"-- (i.e., 2-spaces become tabs, end-line whitespace trimmed)
"nnoremap <silent> <F5> :let _s=@/<Bar>:%s/\s\+$//e<CR>:%s/  /\t/eg<Bar>:let @/=_s<Bar>:nohl<CR>

"-- No eols
:autocmd BufWritePre *.php setlocal binary
:autocmd BufWritePre *.php setlocal noeol
:autocmd BufWritePost *.php setlocal nobinary
