# CRUD
> `<>`는 변수를 의미하고 생성하고 싶은 이름을 넣는 곳

1. 프로젝트 폴더 생성
2. 프로젝트 폴더로 이동 / vscode 실행
    -  `.gitignore` , `README.md` 생성

3. django 프로젝트 생성
    -  `<pjt-name>` 에는 생성하고 싶은 프로젝트의 이름을 작성
```zsh
django-admin startproject <pjt-name> .
```
4. 가상환경 설정
```zsh
python -m venv venv
```

5. 가상환경 활성화
```zsh
source venv/bin/activate
```

6. 가상환경에 django 설치
```zsh
pip install django
```

7. 서버 실행 확인
```zsh
python manage.py runserver
```

8. 앱 생성
```zsh
django-admin startapp <app-name>
```

9. 앱 등록 => `settings.py`
```python
INSTALLED_APPS = [
    ...
    <app_name>,
]
```

10. `url.py` => `views.py` => `templates`


