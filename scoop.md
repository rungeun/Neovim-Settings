# scoop command set

### **⚠ 해당 문서는 Windows PowerShell 5.1 버전을 기준으로 작성되었습니다**
### **⚠ Scoop 설치시에는 관리자 권한이 없이 실행되어야 합니다(보안 관련 문제)**<br>


 이 다음 부터는 Windows PowerShell 5.1을 PowerShell로 지칭함.


## Index
- [scoop command set](#scoop-command-set)
    - [**⚠ 해당 문서는 Windows PowerShell 5.1 버전을 기준으로 작성되었습니다**](#-해당-문서는-windows-powershell-51-버전을-기준으로-작성되었습니다)
    - [**⚠ Scoop 설치시에는 관리자 권한이 없이 실행되어야 합니다(보안 관련 문제)**](#-scoop-설치시에는-관리자-권한이-없이-실행되어야-합니다보안-관련-문제)
  - [Index](#index)
  - [PowerShell 버전 확인하기](#powershell-버전-확인하기)
  - [Scoop 설치](#scoop-설치)
  - [Package 설치](#package-설치)
    - [다음 순서대로 설치](#다음-순서대로-설치)
    - [패키지 설명](#패키지-설명)
  - [Bucket](#bucket)
    - [버킷 설치](#버킷-설치)
    - [설치된 버킷 설명](#설치된-버킷-설명)
  - [기타 명령어](#기타-명령어)
    - [설치한 목록 보기](#설치한-목록-보기)
    - [패키지 찾기 및 설치](#패키지-찾기-및-설치)
    - [패키지 제거](#패키지-제거)
  - [참고문헌:](#참고문헌)
  - [나중에 참고할 문헌:](#나중에-참고할-문헌)


## PowerShell 버전 확인하기
PowerShell 버전을 확인하기 위해 PowerShell 콘솔에`$PSVersionTable`을 입력한 다음 Enter 키를 누릅니다. PSVersion 값을 확인합니다.

>(출력값)
>>
>>Name　　　　 Value
>>                        
>>PSVersion　　　(해당 부분이 5.1이상) <br>
>>PSVersion　　　5.1.19041.3803

[Windows PowerShell 5.1 버전 설치가 필요한 경우](https://learn.microsoft.com/ko-kr/previous-versions/powershell/scripting/windows-powershell/install/installing-windows-powershell?view=powershell-7.1)


## Scoop 설치
⚠ Scoop 설치시에는 관리자 권한이 없이 실행되어야 합니다(보안 관련 문제)
```powershell
> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
> irm get.scoop.sh | iex
```
  
## Package 설치
### 다음 순서대로 설치
```powershell
scoop install 7zip
scoop install aria2
scoop install git
```
### 패키지 설명
`패키지이름`: 설명

예시 설명
```powershell
예시 프로그램
```

---
`7zip` : 고압축을 제공하는 파일 압축 프로그램입니다.

파일 압축: file1.txt와 file2.txt를 archive.7z라는 이름의 압축 파일로 만듭니다. 
```powershell
7z a archive.7z file1.txt file2.txt
```
파일 추출: archive.7z 압축 파일의 내용을 추출합니다.
```powershell
7z x archive.7z
```

---
 `aria2` : 멀티 다운로드, 패키지 여러개를 빠르게 설치

패키지 A-example, B-example, C-example를 한번에 설치하기
```powershell
scoop install sudo A-example, B-example, C-example
```
---
`Git` : 버전 관리 시스템으로, 소프트웨어 개발에서 소스 코드 관리에 사용

(깃 관련 설명은 따로 작성)


## Bucket
 Scoop에서 버킷(Bucket)은 **패키지 모음**을 의미 합니다

(Git 저장소를 통해 패키지 묶음을 가져옴)
### 버킷 설치
예시
```powershell
scoop bucket add <버킷이름>
```
다음 순서대로 설치
```powershell
scoop bucket add main
scoop bucket add extras
scoop bucket add java
scoop bucket add versions
```
### 설치된 버킷 설명
`버킷1` : ~~기능

`버킷1` : ~~기능

[Bucket 목록](https://rasa.github.io/scoop-directory/by-stars)



## 기타 명령어
### 설치한 목록 보기
```powershell
scoop list
```
### 패키지 찾기 및 설치
1. 패키지 찾기
```poqweshell
scoop search <패키지이름>
```
2. sudo로 관리자 권한 부여
```poqweshell
scoop install <패키지이름>
```
3. 권한을 부여하여 설치
```poqweshell
sudo scoop install <패키지이름>
```

### 패키지 제거
```poqweshell
scoop uninstall <패키지이름>
```

[참고 자료](https://github.com/lesstif/scoop-bucket-for-korean)

## 참고문헌: 
[Scoop공식문서](https://github.com/ScoopInstaller/Scoop#readme)

[Bucket](https://rasa.github.io/scoop-directory/by-stars)

[Neovim Setup on Windows](https://www.jasonross.dev/neovim-setup-on-windows-2022/)

## 나중에 참고할 문헌: 
[테마](https://zimmergren.net/making-windows-terminal-look-awesome-with-oh-my-posh/)

[거의 모든 내용이 들어감(터미널,스쿱,테마,아이콘)](https://velog.io/@chanwoo00106/PowerShell-%EA%BE%B8%EB%AF%B8%EA%B8%B0)

[버킷모음(git관련도 있음)](https://github.com/rockerBOO/awesome-neovim?tab=readme-ov-file#git)
