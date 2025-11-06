PS C:\Windows> cd ../../
PS C:\> mkdir Commands


    디렉터리: C:\


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-11-06   오후 5:48                Commands


PS C:\> pwd

Path
----
C:\


PS C:\> cd .\Commands\
PS C:\Commands> mkdir Progects


    디렉터리: C:\Commands


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-11-06   오후 5:49                Progects


PS C:\Commands> ls


    디렉터리: C:\Commands


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-11-06   오후 5:49                Progects


PS C:\Commands> cd ../../
PS C:\> mkdir Logs


    디렉터리: C:\


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-11-06   오후 5:50                Logs


PS C:\> cd  .\Logs\
PS C:\Logs> pwd

Path
----
C:\Logs


PS C:\Logs> cd ../../
PS C:\> mkdir data,reports,backup


    디렉터리: C:\


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-11-06   오후 5:51                data
d-----      2025-11-06   오후 5:51                reports
d-----      2025-11-06   오후 5:51                backup


PS C:\> ls


    디렉터리: C:\


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-05-27   오후 5:58                250527 mh
d-----      2025-11-06   오후 5:51                backup
d-----      2025-11-06   오후 5:49                Commands
d-----      2025-11-06   오후 5:51                data
d-----      2025-11-06  오전 11:13                develops
d-----      2025-11-06   오후 5:50                Logs
d-----      2019-12-07   오후 6:14                PerfLogs
d-r---      2025-10-30  오전 11:25                Program Files
d-r---      2025-09-22  오전 10:17                Program Files (x86)
d-----      2025-11-06   오후 5:51                reports
d-----      2025-05-22  오후 12:56                Temp
d-r---      2025-05-23   오후 5:04                Users
d-----      2025-10-10  오전 11:09                Windows


PS C:\> cd ../../
PS C:\> cd .\Commands .\backup\
Set-Location : '.\backup\' 인수를 허용하는 위치 매개 변수를 찾을 수 없습니다.
위치 줄:1 문자:1
+ cd .\Commands .\backup\
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidArgument: (:) [Set-Location], ParameterBindingException
    + FullyQualifiedErrorId : PositionalParameterNotFound,Microsoft.PowerShell.Commands.SetLocationCommand

PS C:\> cd .\Commands\ .\backup\
Set-Location : '.\backup\' 인수를 허용하는 위치 매개 변수를 찾을 수 없습니다.
위치 줄:1 문자:1
+ cd .\Commands\ .\backup\
+ ~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidArgument: (:) [Set-Location], ParameterBindingException
    + FullyQualifiedErrorId : PositionalParameterNotFound,Microsoft.PowerShell.Commands.SetLocationCommand

PS C:\> cd .\Commands\
PS C:\Commands> pwd

Path
----
C:\Commands


PS C:\Commands> ls


    디렉터리: C:\Commands


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-11-06   오후 5:49                Progects


PS C:\Commands> cd ../../
PS C:\> ls


    디렉터리: C:\


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-05-27   오후 5:58                250527 mh
d-----      2025-11-06   오후 5:51                backup
d-----      2025-11-06   오후 5:49                Commands
d-----      2025-11-06   오후 5:51                data
d-----      2025-11-06  오전 11:13                develops
d-----      2025-11-06   오후 5:50                Logs
d-----      2019-12-07   오후 6:14                PerfLogs
d-r---      2025-10-30  오전 11:25                Program Files
d-r---      2025-09-22  오전 10:17                Program Files (x86)
d-----      2025-11-06   오후 5:51                reports
d-----      2025-05-22  오후 12:56                Temp
d-r---      2025-05-23   오후 5:04                Users
d-----      2025-10-10  오전 11:09                Windows


PS C:\> .\Commands\
.\Commands\ : '.\Commands\' 용어가 cmdlet, 함수, 스크립트 파일 또는 실행할 수 있는 프로그램 이름으로 인식되지 않습니다.
 이름이 정확한지 확인하고 경로가 포함된 경우 경로가 올바른지 검증한 다음 다시 시도하십시오.
위치 줄:1 문자:1
+ .\Commands\
+ ~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (.\Commands\:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException

PS C:\> cd .\Commands\
PS C:\Commands> pwd

Path
----
C:\Commands


PS C:\Commands> pwd

Path
----
C:\Commands


PS C:\Commands> mkdir projects


    디렉터리: C:\Commands


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-11-06   오후 5:56                projects


PS C:\Commands> ls


    디렉터리: C:\Commands


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-11-06   오후 5:49                Progects
d-----      2025-11-06   오후 5:56                projects


PS C:\Commands> mkdir logs


    디렉터리: C:\Commands


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-11-06   오후 5:56                logs


PS C:\Commands> cd .\logs\
PS C:\Commands\logs> pwd

Path
----
C:\Commands\logs


PS C:\Commands\logs> cd ../../
PS C:\> cd .\Commands\
PS C:\Commands> mkdir test


    디렉터리: C:\Commands


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-11-06   오후 5:58                test


PS C:\Commands> mkdir notes


    디렉터리: C:\Commands


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-11-06   오후 5:58                notes


PS C:\Commands> cd .\notes\
PS C:\Commands\notes> cd ../../
PS C:\> .\Commands\
.\Commands\ : '.\Commands\' 용어가 cmdlet, 함수, 스크립트 파일 또는 실행할 수 있는 프로그램 이름으로 인식되지 않습니다.
 이름이 정확한지 확인하고 경로가 포함된 경우 경로가 올바른지 검증한 다음 다시 시도하십시오.
위치 줄:1 문자:1
+ .\Commands\
+ ~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (.\Commands\:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException

PS C:\> cd C
cd : 'C:\C' 경로는 존재하지 않으므로 찾을 수 없습니다.
위치 줄:1 문자:1
+ cd C
+ ~~~~
    + CategoryInfo          : ObjectNotFound: (C:\C:String) [Set-Location], ItemNotFoundException
    + FullyQualifiedErrorId : PathNotFound,Microsoft.PowerShell.Commands.SetLocationCommand

PS C:\> cd .\Commands\
PS C:\Commands> mkdir images,videos,docs


    디렉터리: C:\Commands


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----      2025-11-06   오후 5:59                images
d-----      2025-11-06   오후 5:59                videos
d-----      2025-11-06   오후 5:59                docs


PS C:\Commands> pwd

Path
----
C:\Commands


PS C:\Commands> cd .\docs\
PS C:\Commands\docs> cd ../../
PS C:\>
