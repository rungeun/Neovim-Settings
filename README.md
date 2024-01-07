# Neovim-Settings
The process of downloading and setting up Neovim

>Note: This setting method is based on 2024-01-04
>
>*Warning !: Nothing special*

---
## Index
- [1. 개발툴 설치](#개발툴-설치)
- [2. 홈브루 설치](#홈브루-설치)
- [3. 네오빔 설치](#네오빔-설치)
- [4. 기타 패키지 설치](#기타-패키지-설치)


### Q&A
### References
- [Scoop공식 사이트](https://scoop.sh/)
- [Neovim공식 사이트](https://neovim.io/doc/)

## 개발툴 설치
Microsoft Store를 통해 2개의 프로그램 설치 
>1. Windows Terminal Preview
>
>![캡처](https://github.com/rungeun/Neovim-Settings/assets/132816679/b0c712cd-9573-411a-8a8d-a76a52531746)
>
>2. Ubuntu(WSL)
>
>![ubuntu](https://github.com/rungeun/Neovim-Settings/assets/132816679/32adb9ee-1d22-444f-9d4c-fd971d866c50)

[ 윈도우 설정 ]

1. Windows 기능 켜기/끄기
2. Linux용 Windows 하위 시스템 켜기
3. 재부팅

실행화면
![s](https://github.com/rungeun/Neovim-Settings/assets/132816679/97e40ddf-728c-4e7a-a543-2d9f044c111b)


## 홈브루 설치

`sudo apt update`

`sudo apt-get install build-essential procps curl file git -y`

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`


`test -d ~/.linuxbrew && eval "$(~/.linuxbrew/bin/brew shellenv)"`

`test -d /home/linuxbrew/.linuxbrew && eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"`

`echo "eval \"\$($(brew --prefix)/bin/brew shellenv)\"" >> ~/.bashrc`

## Neovim
`brew install neovim` neovim 패키지 설치

`brew install vim` vim 패키지 설치

## oh my zsh

`brew install zsh` zsh 패키지 설치

` brew install bash`

`sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`  oh-my-zsh 설치

`git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k`

폰트 설정


`nvim ~/.zshrc` 파일을 열어 다음 내용으로 수정 `ZSH_THEME="powerlevel10k/powerlevel10k"`

`source ~/.zshrc`

### zsh 플러그인
zsh-autosuggestions

`git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`

`nvim ~/.zshrc`

`plugins=(git)`에 `zsh-autosuggestions` 추가 ex: `plugins=(git zsh-autosuggestions)`

`source ~/.zshrc` 적용

!아래에도 같은 방법 반복!

zsh-syntax-highlighting

`git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`

web-search

`.zshrc` 파일에만 추가하면 됨


### neovim 플러그인

`mkdir .config` 파일 생성

`cd ~/.config` 파일 이동

`mkdir nvim` 파일 생성

`cd nvim`

`touch init.lua`

`mkdir lua`

`cd lua`

`mkdir rungeun`  mkdir [you name]

`cd rungeun`

`mkdir core`

`mkdir plugins`

`touch plugins-setup.lua`

`cd core`

`touch colorscheme.lua`

`touch keymaps.lua`

`touch options.lua`

`cd ../../../`

여기 앞까지 하나로 묶기 (파일 생성)

`nvim init.lua`

```
require("rungeun.core.options")
require("rungeun.core.keymaps")
require("rungeun.core.colorscheme")
```

## 추가할 내용
터미널창 컴퓨터이름 제거

[a](https://www.youtube.com/watch?v=CF1tMjvHDRA)

[b](https://www.youtube.com/watch?v=vdn_pKJUda8)
