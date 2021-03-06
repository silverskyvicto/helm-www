---
title: "Helm Package"
---

## helm package

차트 디렉토리를 차트 아카이브로 패키징

### 개요


이 명령어는 차트를, 버전이 지정된 차트 아카이브 파일로 패키징한다. 
경로가 지정되면 차트(Chart.yaml 파일을 포함해야 함)에 대한 그 경로를 찾은 다음
해당 디렉토리를 패키징한다.

버전이 지정된 차트 아카이브는 헬름 패키지 저장소에서 사용된다.

차트에 서명하려면 `--sign` 플래그를 사용하자. 대부분의 경우, 
'--keyring path/to/secret/keys' 와 '--key keyname' 도 지정해야 할 것이다.

  $ helm package --sign ./mychart --key mykey --keyring ~/.gnupg/secring.gpg

'--keyring' 을 지정하지 않았고 별다른 설정을 하지 않은 환경이라면
헬름은 보통 공개 키링을 기본값으로 사용한다.


```
helm package [CHART_PATH] [...] [flags]
```

### 옵션

```
      --app-version string   차트의 appVersion 을 이 버전으로 설정
  -u, --dependency-update    패키징 전에 "Chart.yaml" 에서 "charts/" 디렉토리로 의존성 업데이트
  -d, --destination string   차트를 기록할 위치 지정 (기본값 ".")
  -h, --help                 package 에 대한 도움말
      --key string           서명할 때 사용하는 키의 이름. --sign이 true일 경우 사용
      --keyring string       공개 키링의 위치 (기본값 "~/.gnupg/pubring.gpg")
      --sign                 PGP 개인 키를 사용하여 패키지에 서명
      --version string       차트의 버전을 이 유의적(semver) 버전으로 설정
```

### 부모 명령어에서 상속된 옵션들

```
      --add-dir-header                   이 값이 true이면, 헤더에 파일 디렉토리를 추가
      --alsologtostderr                  로그파일처럼 표준오류로도 로그 출력
      --debug                            장황한(verbose) 출력 활성화
      --kube-apiserver string            쿠버네티스 API 서버의 주소 및 포트
      --kube-context string              사용할 kubeconfig 컨텍스트 이름
      --kube-token string                인증에 사용될 베어러(bearer) 토큰
      --kubeconfig string                kubeconfig 파일 경로
      --log-backtrace-at traceLocation   로깅 시 N 행에 걸친 스택 추적 내용을 표시 (기본값 :0)
      --log-dir string                   값을 지정하면, 지정한 디렉토리에 로그 파일 기록
      --log-file string                  값을 지정하면, 지정한 로그 파일 사용
      --log-file-max-size uint           로그파일이 증가할 수 있는 최대 크기 지정. 단위는 메가바이트이다. 값이 0이면, 최대 파일크기는 무제한. (기본값 1800)
      --logtostderr                      로그를 파일이 아닌 표준 출력으로 표시 (기본값 true)
  -n, --namespace string                 요청에 대한 네임스페이스 지정
      --registry-config string           레지스트리 구성 파일에 대한 경로 (기본값 "~/.config/helm/registry.json")
      --repository-cache string          캐시된 저장소 색인이 포함된 파일의 경로 (기본값 "~/.cache/helm/repository")
      --repository-config string         저장소 이름 및 URL 을 포함하는 파일 경로 (기본값 "~/.config/helm/repositories.yaml")
      --skip-headers                     이 값이 true이면, 로그파일에서 헤더 접두어를 미사용
      --skip-log-headers                 이 값이 true이면, 로그파일을 열 때 헤더 제외
      --stderrthreshold severity         stderr로 로그가 변경될 수 있는 최저 임계점 (기본값 2)
  -v, --v Level                          로그 수준 상세표시 레벨
      --vmodule moduleSpec               파일로 필터링된 로깅을 위한 패턴=N 설정의 쉼표로 구분된 리스트
```

### 참조

* [helm](../helm)	 - 쿠버네티스에 대한 헬름 패키지 매니저.

###### Auto generated by spf13/cobra on 11-May-2020
