---
title:  "git push가 안 되는 문제" 
excerpt: "git push가 안 되는 문제"

categories:
  - Git
tags:
  - [Git, Github, git push]

toc: true
toc_sticky: true
 
date: 2023-12-28
last_modified_at: 2023-12-28

---
## git push가 안 되는 문제

상황: 이전에 여러 깃을 연결한 상태에서 다른 깃으로 바꾸는 과정에서 생기는 오류
에러:
remote: Permission to ~.git denied ~
fatal: unable to access ~ : The requested URL returned error: 403

해결 방법 : 

일단 "git config user.name", "git config user.email"을 사용하여 연결된 계정이 동일한 것인지 확인해야 합니다.

다르다면 "git commit"까지는 이상이 없을 것입니다. 이 명령어에서 다른 작성자라고 판단하여 다른 정보에 기록되기 때문입니다.

"git config --global user.email {깃 허브 계정 이메일}"과 같이 --global을 붙히고 깃 허브 계정 이메일을 붙히면 됩니다.



# 1. push 주소에 접근 권한이 없을 경우

bash에서 "git remote -v" 명령어를 통해 경로를 확인합니다.

다른 경우 "git remote set-url https://github.com/깃허브계정이름/레포이름"를 사용하여 경로를 맞춰줍니다.

# 2. 기존 계정과 다른 계정으로 push를 할 때

위치 : 설정 - 제어판 - 자격 증명 관리자
자격 증명 관리자 아래, 일반 자격 증명에 github 주소가 최초로 연결했던 github계정입니다. 제가 바꾸고 싶은 계정으로 바꾸면 됩니다.

# 3. 
