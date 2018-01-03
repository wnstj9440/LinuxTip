# LinuxTip

* bash에서 tab 누를때 대소문자 구분 없이 자동완성하기
	* /etc/inputrc 파일에 __set completion-ignore-case on__ 추가

* Node.js Upgrade
	1. sudo npm cache clean -f		: 캐시 강제 삭제
	2. sudo npm install -g n		: n 모듈 설치
	3. sudo n stable					: n 모듈 이용하여 Node.js 설치

* vim 마크다운 liveview 플러그인 설치
	1. git clone git://github.com/shime/vim-livedown.git ~/.vim/bundle/vim-livedown 
	2. vimrc 파일에 __Plugin 'shime/vim-livedown'__ 추가
	3. __:so %__ 실행(vimrc 적용) 후  __:PluginInstall__ 실행
	4. npm install -g livedown    (nodejs 4.5.0 이상 버전)
	5. Usage
		* :LivedownPreview  	-> Preview start
		* :LivedownKill		-> Preview end
		* :LivedownToggle		-> Preview toggle
