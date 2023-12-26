# scoop command set

<br>

### **⚠ 해당 문서는 Windows PowerShell 5.1 버전을 기준으로 작성되었습니다**
### **⚠ Scoop 설치시에는 관리자 권한이 없이 실행되어야 합니다(보안 관련 문제)**
<br>

---

이 다음 부터는 Windows PowerShell 5.1을 PowerShell로 지칭함.
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
```powershell
> Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
> irm get.scoop.sh | iex
```

## Butkit 설치

[Butkit 목록](https://rasa.github.io/scoop-directory/by-stars)

## 




















<br>
<br>
<br>

## 참고문헌: 
[Scoop공식문서](https://github.com/ScoopInstaller/Scoop#readme)

[Bukkit](https://rasa.github.io/scoop-directory/by-stars)