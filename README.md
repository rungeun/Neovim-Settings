# Neovim-Settings
The process of downloading and setting up Neovim
>(How to use neovim using Windows PowerShell)
>
>Note: This setting method is based on 2023-12-25
>
>*Warning !: Nothing special*

---
## Index
###  Neovim
- [1. Windows PowerShell Settings](#Windows-PowerShell-Settings)
- [2. Install Scoop](#)
- [3. Download and Install Neovim -Scoop](#Download-and-Install-Neovim--Scoop)
- [4. Setting Environment Variables](#Setting-Environment-Variables)
- [5. Additional Configuration and Customization](#Additional-Configuration-and-Customization)
- [6. powershell git push](#)

### Q&A
### References
- [Scoop공식 사이트](https://scoop.sh/)

---
# Neovim
- ## Windows-PowerShell-Settings
### PowerShell 실행 
`Windows PowerShell` 관리자 권한으로 실행
>
### PowerShell 색상 변경하기
창 상단바를 우클릭하여 `속성`클릭
>
`색`에 `화면 배경`을 블랙으로 변경후 `완료` 클릭
>
### Scoop 설치
```powershell
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
iwr -useb get.scoop.sh | iex
```


