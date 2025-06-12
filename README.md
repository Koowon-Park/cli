#__프로젝트 요약:__

이 프로젝트는 Go 언어로 작성된 CLI (Command Line Interface) 애플리케이션을 만들기 위한 프레임워크인 `urfave/cli`입니다. 주요 특징은 선언적, 간단함, 빠름, 재미입니다. 명령어 및 하위 명령어, 유연한 도움말 시스템, 동적 셸 자동 완성, 다양한 입력 플래그를 지원하며, Go 표준 라이브러리 외에는 의존성이 없습니다. 주요 파일은 `cli.go`, `command.go`, `flag.go`, `go.mod`, `README.md`이며, 테스트, Markdown 변환, YAML 파싱 등의 의존성을 가지고 있습니다.

- __선언적__: CLI 애플리케이션을 쉽게 정의하고 구성할 수 있습니다.
- __간단함__: 이해하고 작성하기 쉬운 API를 제공합니다.
- __빠름__: Go 언어의 성능을 활용하여 빠른 실행 속도를 제공합니다.
- __재미__: 개발자가 즐겁게 CLI 애플리케이션을 만들 수 있도록 설계되었습니다.

##__주요 기능:__

- 명령어 및 하위 명령어 지원 (alias 및 prefix 매칭 지원)

- 유연하고 관대한 도움말 시스템

- `bash`, `zsh`, `fish`, `powershell`에 대한 동적 셸 자동 완성

- Go 표준 라이브러리 외에는 의존성이 없음

- 단순 타입, 단순 타입 슬라이스, 시간, 기간 등에 대한 입력 플래그

- 복합 짧은 플래그 지원 (`-a` `-b` `-c`를 `-abc`로 단축 가능)

- `man` 및 Markdown 형식의 문서 생성 ([`urfave/cli-docs`][urfave/cli-docs] 모듈을 통해 지원)

- 다음 소스에서 입력 조회:

  - 환경 변수
  - 일반 텍스트 파일
  - 구조화된 파일 형식 ([`urfave/cli-altsrc`][urfave/cli-altsrc] 모듈을 통해 지원)

##__주요 파일:__

- `cli.go`: CLI 애플리케이션의 기본 구조와 실행 로직을 정의합니다.
- `command.go`: 명령어의 구조, 플래그, 실행 함수 등을 정의합니다.
- `flag.go`: 플래그의 종류, 옵션, 유효성 검사 등을 정의합니다.
- `go.mod`: 프로젝트의 의존성 정보를 관리합니다.
- `README.md`: 프로젝트에 대한 전반적인 정보와 사용법을 제공합니다.

__의존성:__

- `github.com/stretchr/testify`: 테스트를 위한 어설션 라이브러리
- `github.com/cpuguy83/go-md2man/v2`: Markdown을 man 페이지로 변환하는 라이브러리
- `github.com/davecgh/go-spew`: Go 데이터 구조를 검사하는 라이브러리
- `github.com/pmezard/go-difflib`: diff 계산 라이브러리
- `github.com/russross/blackfriday/v2`: Markdown 파서 라이브러리
- `github.com/urfave/cli/v2`: 이전 버전의 `urfave/cli` 라이브러리 (간접 의존성)
- `github.com/xrash/smetrics`: 문자열 유사성 측정 라이브러리
- `gopkg.in/yaml.v3`: YAML 파싱 라이브러리



# Welcome to urfave/cli

[![Go Reference][goreference_badge]][goreference_link]
[![Go Report Card][goreportcard_badge]][goreportcard_link]
[![codecov][codecov_badge]][codecov_link]
[![Tests status][test_badge]][test_link]

urfave/cli is a **declarative**, simple, fast, and fun package for building
command line tools in Go featuring:

- commands and subcommands with alias and prefix match support
- flexible and permissive help system
- dynamic shell completion for `bash`, `zsh`, `fish`, and `powershell`
- no dependencies except Go standard library
- input flags for simple types, slices of simple types, time, duration, and
  others
- compound short flag support (`-a` `-b` `-c` can be shortened to `-abc`)
- documentation generation in `man` and Markdown (supported via the
  [`urfave/cli-docs`][urfave/cli-docs] module)
- input lookup from:
  - environment variables
  - plain text files
  - structured file formats (supported via the
    [`urfave/cli-altsrc`][urfave/cli-altsrc] module)

## Documentation

See the hosted documentation website at <https://cli.urfave.org>. Contents of
this website are built from the [`./docs`](./docs) directory.

## Support

Check the [Q&A discussions]. If you don't find answer to your question, [create
a new discussion].

If you found a bug or have a feature request, [create a new issue].

Please keep in mind that this project is run by unpaid volunteers.

### License

See [`LICENSE`](./LICENSE).

[test_badge]: https://github.com/urfave/cli/actions/workflows/test.yml/badge.svg
[test_link]: https://github.com/urfave/cli/actions/workflows/test.yml
[goreference_badge]: https://pkg.go.dev/badge/github.com/urfave/cli/v3.svg
[goreference_link]: https://pkg.go.dev/github.com/urfave/cli/v3
[goreportcard_badge]: https://goreportcard.com/badge/github.com/urfave/cli/v3
[goreportcard_link]: https://goreportcard.com/report/github.com/urfave/cli/v3
[codecov_badge]: https://codecov.io/gh/urfave/cli/branch/main/graph/badge.svg?token=t9YGWLh05g
[codecov_link]: https://codecov.io/gh/urfave/cli
[Q&A discussions]: https://github.com/urfave/cli/discussions/categories/q-a
[create a new discussion]: https://github.com/urfave/cli/discussions/new?category=q-a
[urfave/cli-docs]: https://github.com/urfave/cli-docs
[urfave/cli-altsrc]: https://github.com/urfave/cli-altsrc
[create a new issue]: https://github.com/urfave/cli/issues/new/choose
