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

10. `url.py` => `views.py` => `templates/*.html` 순서로 코드 작성



## Model

1. 모델 정의 (`models.py`)
    - 모델의 이름은 기본적으로 단수형태

```python
from django.db import models

class Post(models.Model):
    title = models.CharField(max_length=100)
    content = models.TextField()
```

2. 번역본 생성
```zsh
python manage.py makemigrations
```

3. DB에 반열
```zsh
python manage.py migrate
```

4. SQL 스키마 확인
```zsh
python manage.py sqlmigrate posts 0001
```

5. 생성한 모델 admin에 등록
```python
from django.contrib import admin
from .models import Post

admin.site.register(Post)
```

6. 관리자 계정 생성
```zsh
python manage.py createsuperuser
```


## CRUD 로직 작성

### 1. Read
- 전체 게시물 출력
```python

``` 

- 하나의 게시물 출력
```python

```


### 2. Create
- 사용자에게 입력할 수 있는 폼을 제공
```python
```

- 사용자가 입력한 데이터를 가지고 DB에 저장하는 로직
```python
```

### 3. Delete

### 4. Update