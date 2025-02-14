OmniOneID.github.io
==

Welcome to OmniOneID.github.io Repository. <br>
This repository contains the source code, and related resources for OmniOneID.github.io.

본 프로젝트는 OmniOne OpenDID의 아키텍쳐 문서에 대한 서빙을 GitHub Pages 기술을 기반으로 제공합니다.
GitHub Pages에 대한 기술 가이드는 [GitHub Pages](https://docs.github.com/en/pages)를 참조해주십시요.

## Maintaining Guide
좌측의 사이드바는 [docsify.js](https://docsify.js.org/)의 기본 규칙에 따라 sidebar.md를 기준으로 관리됩니다.
사이드바는 언어별 그리고 버전별로 따로 관리되며, [sidebar 브랜치](https://github.com/OmniOneID/did-doc-architecture/tree/sidebar/)를 기준으로 관리됩니다.
버전이 올라갈 때마다 maintainer는 새로운 기준의 문서 목차를 검토한 후 해당 버전에 맞는 sidebar.md를 생성합니다.
쉬운 sidebar.md의 생성을 위해서는 [docsify-cli](https://github.com/docsifyjs/docsify-cli)를 활용할 수 있습니다.
- 상단의 네비게이션바 또한 navbar.md 기준으로 관리되며 sidebar 브랜치에 존재합니다.
- 버전이 추가되면 index.html 내부의 alias 설정 추가가 필요합니다.
 
```java
alias: { // custom setting
  '/V1.0.0/(.*)': getRawGithubUserContentURL() + '/refs/heads/V1.0.0/$1',
  '/V1.1.0/(.*)': getRawGithubUserContentURL() + '/refs/heads/V1.1.0/$1'
},
```

## Contributing
Please read [CONTRIBUTING.md](CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) for details on our code of conduct, and the process for submitting pull requests to us.

## License
[Apache 2.0](LICENSE)
