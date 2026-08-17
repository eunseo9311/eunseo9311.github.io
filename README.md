# Eunseo Song — Researcher Website

Eunseo Song의 Jekyll 기반 개인 연구자 홈페이지입니다. 공개 콘텐츠는 `index.md` 한 페이지에 있으며 Biography, 연락처/프로필 아이콘, Research Interest, Education, Work Experiences 순서로 구성됩니다. 프로필 사진은 `EunseoSong.JPG`를 사용합니다.

## 콘텐츠 수정

- 본문과 링크: `index.md`
- 이름, 사이트 주소, 프로필 사진 경로: `_config.yml`
- 공통 레이아웃: `_layouts/default.html`
- 디자인: `_sass/`
- 연락처 아이콘: `assets/icons/`

현재 CV, Publications, Projects, Open Source Contributions, Awards 섹션은 없습니다. CV PDF가 준비되면 파일을 저장소에 추가한 뒤 이름 아래에 다음과 같은 한 줄을 추가할 수 있습니다.

```markdown
* [CV]({{ '/assets/files/cv.pdf' | relative_url }})
```

## 로컬 실행

Ruby와 Bundler가 설치된 환경에서 다음 명령을 실행합니다.

```sh
bundle install
bundle exec jekyll serve
```

브라우저에서 <http://localhost:4000>을 엽니다. 배포 환경과 같은 프로덕션 빌드는 다음과 같이 검사합니다.

```sh
JEKYLL_ENV=production bundle exec jekyll build
```

## GitHub Pages 배포

사용자 사이트용 저장소는 `eunseo9311.github.io`라는 이름으로 생성하고 코드를 올립니다. GitHub 저장소의 **Settings → Pages**에서 배포 브랜치와 `/ (root)`를 선택합니다. 현재 `_config.yml`은 사용자 사이트에 맞춰 다음 값으로 설정되어 있습니다.

```yaml
url: "https://eunseo9311.github.io"
baseurl: ""
```

실제 저장소를 다른 이름으로 만들면 프로젝트 사이트 규칙에 맞게 `url`과 `baseurl`을 수정해야 합니다. 비밀번호, API 키 등 비밀값은 저장소에 커밋하지 마세요.
