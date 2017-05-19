## [Help Maintain Vundle](https://github.com/VundleVim/Vundle.vim/issues/383)

## About

[Vundle] is short for _Vim bundle_ and is a [Vim] plugin manager.

[Vundle] allows you to...

* keep track of and [configure] your plugins right in the `.vimrc`
* [install] configured plugins (a.k.a. scripts/bundle)
* [update] configured plugins
* [search] by name all available [Vim scripts]
* [clean] unused plugins up
* run the above actions in a *single keypress* with [interactive mode]

[Vundle] automatically...

* manages the [runtime path] of your installed scripts
* regenerates [help tags] after installing and updating

[Vundle] is undergoing an [interface change], please stay up to date to get latest changes.

[![Gitter-chat](https://badges.gitter.im/VundleVim/Vundle.vim.svg)](https://gitter.im/VundleVim/Vundle.vim) for discussion and support.

![Vundle-installer](http://i.imgur.com/Rueh7Cc.png)

## Quick Start

1. Introduction:

   Installation requires [Git] and triggers [`git clone`] for each configured repository to `~/.vim/bundle/` by default.
   Curl is required for search.

   If you are using Windows, go directly to [Windows setup]. If you run into any issues, please consult the [FAQ].
   See [Tips] for some advanced configurations.

   Using non-POSIX shells, such as the popular Fish shell, requires additional setup. Please check the [FAQ].

2. Set up [Vundle]:

   `$ git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim`

3. Configure Plugins:

   Put this at the top of your `.vimrc` to use Vundle. Remove plugins you don't need, they are for illustration purposes.

   ```vim
   set nocompatible              " be iMproved, required
   filetype off                  " required

   " set the runtime path to include Vundle and initialize
   set rtp+=~/.vim/bundle/Vundle.vim
   call vundle#begin()
   " alternatively, pass a path where Vundle should install plugins
   "call vundle#begin('~/some/path/here')

   " let Vundle manage Vundle, required
   Plugin 'VundleVim/Vundle.vim'

   " The following are examples of different formats supported.
   " Keep Plugin commands between vundle#begin/end.
   " plugin on GitHub repo
   Plugin 'tpope/vim-fugitive'
   " plugin from http://vim-scripts.org/vim/scripts.html
   " Plugin 'L9'
   " Git plugin not hosted on GitHub
   Plugin 'git://git.wincent.com/command-t.git'
   " git repos on your local machine (i.e. when working on your own plugin)
   Plugin 'file:///home/gmarik/path/to/plugin'
   " The sparkup vim script is in a subdirectory of this repo called vim.
   " Pass the path to set the runtimepath properly.
   Plugin 'rstacruz/sparkup', {'rtp': 'vim/'}
   " Install L9 and avoid a Naming conflict if you've already installed a
   " different version somewhere else.
   " Plugin 'ascenator/L9', {'name': 'newL9'}

   " All of your Plugins must be added before the following line
   call vundle#end()            " required
   filetype plugin indent on    " required
   " To ignore plugin indent changes, instead use:
   "filetype plugin on
   "
   " Brief help
   " :PluginList       - lists configured plugins
   " :PluginInstall    - installs plugins; append `!` to update or just :PluginUpdate
   " :PluginSearch foo - searches for foo; append `!` to refresh local cache
   " :PluginClean      - confirms removal of unused plugins; append `!` to auto-approve removal
   "
   " see :h vundle for more details or wiki for FAQ
   " Put your non-Plugin stuff after this line
   ```

4. 플러그인 설치:

   `vim`을 켠 후 `:PluginInstall`을 실행하세요

   명령줄에서 설치: `vim +PluginInstall +qall`

5. (선택) fish shell 사용시: `.vimrc`내에 `set shell=/bin/bash`을 추가하세요

## 문서

더 자세한 내용은 [`:h vundle`](https://github.com/VundleVim/Vundle.vim/blob/master/doc/vundle.txt) 문서를 참조하세요.

## 변경기록

[변경기록](https://github.com/VundleVim/Vundle.vim/blob/master/changelog.md)을 확인하세요.

## Vundle을 사용하는 사람들

[예시](https://github.com/VundleVim/Vundle.vim/wiki/Examples)를 확인하세요.

## 기여자

[Vundle 기여자 명단](https://github.com/VundleVim/Vundle.vim/graphs/contributors)을 확인하세요.

*감사합니다!*

## 아이디어 및 영감

* [pathogen.vim](http://github.com/tpope/vim-pathogen/)
* [Bundler](https://github.com/bundler/bundler)
* [Scott Bronson](http://github.com/bronson)

## 기타

* Vundle은 [Vim] 버젼 7.3으로 OS X, Linux 및 Windows에서 개발 및 테스트 되었습니다.
* Vundle은 최대한 [KISS](http://en.wikipedia.org/wiki/KISS_principle) 원칙을 준수합니다.

## 할일:
[Vundle]은 현재 개발이 진행 중 입니다. 그러니 어떤 아이디어이든 개선점이든 알려주시면 감사하겠습니다.

* [x] `:PluginInstall`을 실행하거나 재실행 하였을 때 새로 추가된 플러그인들을 `.vimrc`에 새롭게 추가하는 기능 활성화
* [x] 미리보기 창에 검색 결과 띄우기
* [x] Vim 문서 작성
* [x] `bundles/`에 Vundle넣기 (Vundle 도움말이 수정됨)
* [x] 테스트
* [x] 에러 관리 개선
* [ ] 각 수정 및 버전의 명시를 가능하게?
* [ ] 의존성 관리
* [ ] 검색 결과에 설명 보여주기
* [ ] 설명으로 검색하기
* [ ] 존나 쩔게 만들기!

[Vundle]:http://github.com/VundleVim/Vundle.vim
[Windows setup]:https://github.com/VundleVim/Vundle.vim/wiki/Vundle-for-Windows
[FAQ]:https://github.com/VundleVim/Vundle.vim/wiki
[Tips]:https://github.com/VundleVim/Vundle.vim/wiki/Tips-and-Tricks
[Vim]:http://www.vim.org
[Git]:http://git-scm.com
[`git clone`]:http://gitref.org/creating/#clone

[Vim scripts]:http://vim-scripts.org/vim/scripts.html
[help tags]:http://vimdoc.sourceforge.net/htmldoc/helphelp.html#:helptags
[runtime path]:http://vimdoc.sourceforge.net/htmldoc/options.html#%27runtimepath%27

[configure]:https://github.com/VundleVim/Vundle.vim/blob/v0.10.2/doc/vundle.txt#L126-L233
[install]:https://github.com/VundleVim/Vundle.vim/blob/v0.10.2/doc/vundle.txt#L234-L254
[update]:https://github.com/VundleVim/Vundle.vim/blob/v0.10.2/doc/vundle.txt#L255-L265
[search]:https://github.com/VundleVim/Vundle.vim/blob/v0.10.2/doc/vundle.txt#L266-L295
[clean]:https://github.com/VundleVim/Vundle.vim/blob/v0.10.2/doc/vundle.txt#L303-L318
[interactive mode]:https://github.com/VundleVim/Vundle.vim/blob/v0.10.2/doc/vundle.txt#L319-L360
[interface change]:https://github.com/VundleVim/Vundle.vim/blob/v0.10.2/doc/vundle.txt#L372-L396
