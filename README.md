# 🖼️ Python & Android Image Blog

Django 기반 Python Image Blog 백엔드와 Android 클라이언트 앱이 함께 포함되어 있습니다. 학습용/샘플용으로 이미지 업로드, 게시글 작성·수정·삭제, 검색 기능 등 을 제공합니다.

## 📂 프로젝트 구성
### 1️⃣ Python Image Blog (백엔드)
```bash
django-imageBlog/
├── README.md
├── .gitignore
├── mysite/
│   ├── manage.py
│   ├── db.sqlite3
│   ├── venv/
│   ├── mysite/
│   └── blog/
│       ├── models.py
│       ├── views.py
│       ├── serializers.py
│       └── templates/static/
```

### 2️⃣ Android 클라이언트
```bash
ImageBlog-Android/
├── README.md
├── app/
│   ├── build.gradle
│   └── src/main/java/com/example/imageblog/
│       ├── MainActivate.java
│       ├── NewPostActivity.java
│       ├── PostDetailActivity.java
│       ├── NetworkClient.java
│       ├── AuthInterceptor.java
│       └── AuthHelper.java
```

### 참고
- 백엔드 GitHub: [django-imageBlog](https://github.com/seohyunlee-coding/django-imageBlog)
- Android 클라이언트 GitHub: [seohyunlee-coding-django-imageBlog-Android](https://github.com/seohyunlee-coding/seohyunlee-coding-django-imageBlog-Android)

## ⚙️ 설치 및 실행
### 1️⃣ Python Image Blog (백엔드)
### Python 버전 확인
```bash
python --version
# Python 3.13 이상
```

### 프로젝트 클론
```bash
git clone https://github.com/seohyunlee-coding/Python-Image-Blog
cd django-imageBlog/mysite
```

### 가상환경 생성 및 활성화 (Windows)
```bash
python -m venv .\venv
venv\Scripts\activate
```

### 데이터베이스 마이그레이션
```bash
python manage.py migrate
```

### 개발 서버 실행
```bash
python manage.py runserver
```
- 로컬 서버: http://127.0.0.1:8000/
- PythonAnywhere 배포: https://cwijiq.pythonanywhere.com/

### 2️⃣ Android 클라이언트
### 개발 환경
- Android Studio 최신 안정화 버전
- Android SDK
- Java 11 이상
- Django REST API 서버 실행 필요

### 빌드 및 실행
- Android Studio → Open → ImageBlog-Android 폴더 선택

### 명령줄 빌드:
```bash
cd "C:\Users\dev\Desktop\ImageBlog-Android"
gradlew.bat assembleDebug
```
- 에뮬레이터 또는 물리 디바이스에서 실행


## 🚀 주요 기능
### 공통 기능
- 게시글 목록 조회
- 게시글 상세 보기(이미지 포함)
- 게시글 생성/수정/삭제
- 게시글 검색
- Token 기반 인증

### 백엔드 API 엔드포인트
| 기능             | 메서드 | URL                          |
|----------------|--------|-----------------------------|
| 토큰 발급        | POST   | /api-token-auth/            |
| 게시글 목록 조회  | GET    | /api/posts                  |
| 게시글 생성      | POST   | /api_root/Post/             |
| 게시글 수정      | PATCH  | /api_root/Post/{id}/        |
| 게시글 삭제      | DELETE | /api_root/Post/{id}/        |
| 게시글 검색      | GET    | /api/posts/search/?q={query} |


## 🛠️ 사용 기술
### 백엔드
- Python 3.13, Django 5.27, Django REST Framework
- Pillow (이미지 처리)
- curl (API 테스트)
- PythonAnywhere 배포

### Android 클라이언트
- Android (Java)
- OkHttp, Glide
- AndroidX, Material Components

## 🐛 버그 / 디버그 팁

- 이미지 업로드 시 파일 경로/이름 확인
- DRF API에서 author는 정수 PK 필요
- Pillow 설치 누락 시 ImageField 오류
- 토큰 인증 문제 시 토큰 재발급
  
## 📚 참고 / 출처
- [Django 공식 문서](https://docs.djangoproject.com/en/5.2/)
- [Django REST Framework](https://www.django-rest-framework.org/)
- [Pillow 문서](https://pillow.readthedocs.io/en/stable/)
- PythonAnywhere 배포: https://cwijiq.pythonanywhere.com/

## 👩‍💻 작성자 / 연락처
- 이름: 이서현
- 이메일: cwijiq3085@gmail.com
- GitHub: [seohyunlee-coding](https://github.com/seohyunlee-coding)
