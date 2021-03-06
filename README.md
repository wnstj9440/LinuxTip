# LinuxTip

* bash에서 tab 누를때 대소문자 구분 없이 자동완성하기
<pre>
 /etc/inputrc 파일에 __set completion-ignore-case on__ 추가
</pre>
<hr/>

* Advanced-cp, mv (복사, 이동 중 Progress bar 표시) -> root user에서 설치
	1. wget https://www.dropbox.com/s/o9rs7o0l0569iv3/coreutils-8.4-receipt.tar.gz?dl=0
	2. mv -v coreutils-8.4-receipt.tar.gz?dl=0 coreutils-8.4-receipt.tar.gz
	3. tar -zxvf coreutils-8.4-receipt.tar.gz 
	4. tar -zxvf coreutils-8.4.tar.gz
	5. cp -v coreutils-8.4.patch coreutils-8.4/
	6. cd coreutils-8.4/
	7. patch -p1 -i coreutils-8.4.patch
	8. ./configure 
	9. make
	10. cp src/cp /usr/local/bin/cp; cp src/mv /usr/local/bin/mv   (cp와 mv경로는 which 명령을 통해 확인)
<hr/>


```
```

* Node.js Upgrade
	1. sudo npm cache clean -f		: 캐시 강제 삭제
	2. sudo npm install -g n		: n 모듈 설치
	3. sudo n stable					: n 모듈 이용하여 Node.js 설치
<hr/>

* vim vundle 설치
	1. git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim
	2. vimrc 첫 부분에 아래 내용 추가
<pre><code>set nocompatible
filetype off

set rtp+=~/.vim/bundle/Vundle.vim

call vundle#begin()
	Plugin 'VundleVim/Vundle.vim'
call vundle#end()
</code></pre>
<hr/>

* vim 명령 단축키 설정
<pre>
 nmap <단축키>:LivedownToggle<CR>
 ex) nmap gm:LivedownToggle<CR>
</pre>
<hr/>

* vim 마크다운 liveview 플러그인 설치
<pre>
 1. git clone git://github.com/shime/vim-livedown.git ~/.vim/bundle/vim-livedown 
 2. vimrc 파일에 __Plugin 'shime/vim-livedown'__ 추가
 3. __:so %__ 실행(vimrc 적용) 후  __:PluginInstall__ 실행
 4. npm install -g livedown    (nodejs 4.5.0 이상 버전)
 5. Usage
   :LivedownPreview 		-> Preview start
   :LivedownKill		-> Preview end
   :LivedownToggle		-> Preview toggle
</pre>
