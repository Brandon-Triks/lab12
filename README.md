# Лабораторная работа 12  
Цель данной лабораторной работы: ознакомиться с специализированным текстовым редактором Vim.  
# Шаг 1 - Установка VIM  
```bash
igor@debian:~/Brandon-Triks/workspace/projects/lab12$ sudo apt install vim -y
[sudo] пароль для igor: 
Установка:                                                        
  vim

Установка зависимостей:
  vim-runtime

Предлагаемые пакеты:
  ctags  vim-doc  vim-scripts

Сводка:
  Обновление: 0, Установка: 2, Удаление: 0, Пропуск обновления: 198
  Объём загрузки: 8 797 kB
  Требуемое пространство: 43,4 MB / 17,8 GB доступно

Пол:1 http://deb.debian.org/debian trixie/main amd64 vim-runtime all 2:9.1.1230-2 [7 127 kB]
Пол:2 http://deb.debian.org/debian trixie/main amd64 vim amd64 2:9.1.1230-2 [1 670 kB]
Получено 8 797 kB за 2с (4 942 kB/s)
Выбор ранее не выбранного пакета vim-runtime.
(Чтение базы данных … на данный момент установлено 151166 файлов и каталогов.)
Подготовка к распаковке …/vim-runtime_2%3a9.1.1230-2_all.deb …
Добавляется «отклонение /usr/share/vim/vim91/doc/help.txt в /usr/share/vim/vim91
/doc/help.txt.vim-tiny из-за vim-runtime»
Добавляется «отклонение /usr/share/vim/vim91/doc/tags в /usr/share/vim/vim91/doc
/tags.vim-tiny из-за vim-runtime»
Распаковывается vim-runtime (2:9.1.1230-2) …
Выбор ранее не выбранного пакета vim.
Подготовка к распаковке …/vim_2%3a9.1.1230-2_amd64.deb …
Распаковывается vim (2:9.1.1230-2) …
Настраивается пакет vim-runtime (2:9.1.1230-2) …
Настраивается пакет vim (2:9.1.1230-2) …
update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin
/ex (ex) в автоматическом режиме
update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin
/rview (rview) в автоматическом режиме
update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin
/rvim (rvim) в автоматическом режиме
update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin
/vi (vi) в автоматическом режиме
update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin
/view (view) в автоматическом режиме
update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin
/vim (vim) в автоматическом режиме
update-alternatives: используется /usr/bin/vim.basic для предоставления /usr/bin
/vimdiff (vimdiff) в автоматическом режиме
Обрабатываются триггеры для man-db (2.13.1-1) …
igor@debian:~/Brandon-Triks/workspace/projects/lab12$ vim --version
VIM - Vi IMproved 9.1 (2024 Jan 02, сборка от May 23 2025 00:48:59)
Исправления: 1-948, 950-1230, 1242, 1244
С изменениями, внесёнными team+vim@tracker.debian.org
Скомпилирована team+vim@tracker.debian.org
Максимальная версия без графического интерфейса.
 В этой версии включены (+) и отключены (-) следующие компоненты:
+acl               +file_in_path      +mouse_urxvt       -tag_any_white
+arabic            +find_in_path      +mouse_xterm       -tcl
+autocmd           +float             +multi_byte        +termguicolors
+autochdir         +folding           +multi_lang        +terminal
-autoservername    -footer            -mzscheme          +terminfo
-balloon_eval      +fork()            +netbeans_intg     +termresponse
+balloon_eval_term +gettext           +num64             +textobjects
-browse            -hangul_input      +packages          +textprop
++builtin_terms    +iconv             +path_extra        +timers
+byte_offset       +insert_expand     -perl              +title
+channel           +ipv6              +persistent_undo   -toolbar
+cindent           +job               +popupwin          +user_commands
-clientserver      +jumplist          +postscript        +vartabs
-clipboard         +keymap            +printer           +vertsplit
+cmdline_compl     +lambda            +profile           +vim9script
+cmdline_hist      +langmap           -python            +viminfo
+cmdline_info      +libcall           -python3           +virtualedit
+comments          +linebreak         +quickfix          +visual
+conceal           +lispindent        +reltime           +visualextra
+cryptv            +listcmds          +rightleft         +vreplace
+cscope            +localmap          -ruby              +wildignore
+cursorbind        -lua               +scrollbind        +wildmenu
+cursorshape       +menu              +signs             +windows
+dialog_con        +mksession         +smartindent       +writebackup
+diff              +modify_fname      +sodium            -X11
+digraphs          +mouse             -sound             +xattr
-dnd               -mouseshape        +spell             -xfontset
-ebcdic            +mouse_dec         +startuptime       -xim
+emacs_tags        +mouse_gpm         +statusline        -xpm
+eval              -mouse_jsbterm     -sun_workshop      -xsmp
+ex_extra          +mouse_netterm     +syntax            -xterm_clipboard
+extra_search      +mouse_sgr         +tag_binary        -xterm_save
-farsi             -mouse_sysmouse    -tag_old_static    
           общесистемный файл vimrc: "/etc/vim/vimrc"
   1-ый пользовательский файл vimrc: "$HOME/.vimrc"
   2-ой пользовательский файл vimrc: "~/.vim/vimrc"
   3-ий пользовательский файл vimrc: "
$XDG_CONFIG_HOME/vim/vimrc"
    1-ый пользовательский файл exrc: "$HOME/.exrc"
    файл предустановленных настроек: "
$VIMRUNTIME/defaults.vim"
         значение $VIM по умолчанию: "/usr/share/vim"
Параметры сборки: gcc -c -I. -Iproto -DHAVE_CONFIG_H -Wdate-time -g -O2 -Werror=implicit-function-declaration -ffile-prefix-map=/build/reproducible-path/vim-9.1.1230=. -fstack-protector-strong -fstack-clash-protection -Wformat -Werror=format-security -fcf-protection -DSYS_VIMRC_FILE=\"/etc/vim/vimrc\" -DSYS_GVIMRC_FILE=\"/etc/vim/gvimrc\" -D_REENTRANT -U_FORTIFY_SOURCE -D_FORTIFY_SOURCE=1 
Связывание: gcc -Wl,-z,relro -Wl,-z,now -Wl,--as-needed -o vim -lm -ltinfo -lselinux -lsodium -lacl -lattr -lgpm 
```  
## Шаг 2 - выполнение туториала самого текстового редактора  
```bash
igor@debian:~/Brandon-Triks/workspace/projects/lab12$ vimtutor ru
```  
## Вывод  
В ходе работы были получены базовые навыки работы с Vim такие, как: перемещение по текст, переход в режим вставки, удаление символов,сохранение файла,выход из редактора
