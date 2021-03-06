---
title: "Helm Dependency Build"
---

## helm dependency build

Chart.lock 파일을 기반으로 charts/ 디렉토리를 다시 빌드

### 개요


Chart.lock 파일에서 charts/ 디렉토리를 빌드한다.

빌드는 잠금파일에 지정된 상태에 대한 차트의 종속성을 재구성하는데
사용된다. 이것은 'helm dependency update' 처럼 
종속성을 다시 재협상하지 않는다.

잠금 파일이 없으면 'helm dependency build'는 
'helm dependency update'의 동작을 미러링합니다.



```
helm dependency build CHART [flags]
```

### 옵션

```
  -h, --help             helm dependency build 명령어에 대한 도움말
      --keyring string   공개 키를 포함하는 키링 (기본값 "~/.gnupg/pubring.gpg")
      --verify           서명과 비교하여 패키지 확인
```

### 부모 명령어에서 상속된 옵션들

```
      --debug                       장황한(verbose) 출력 활성화
      --kube-apiserver string       쿠버네티스 API 서버의 주소 및 포트
      --kube-as-group stringArray   작업에 관해 제시할 그룹. 플래그를 여러 번 사용하여 여러 그룹 지정 가능
      --kube-as-user string         작업에 관해 제시할 사용자명
      --kube-context string         사용할 kubeconfig 컨텍스트 이름
      --kube-token string           인증에 사용될 베어러(bearer) 토큰
      --kubeconfig string           kubeconfig 파일 경로
  -n, --namespace string            이 요청에 대한 네임스페이스 스코프
      --registry-config string      레지스트리 구성 파일에 대한 경로 (기본값 "~/.config/helm/registry.json")
      --repository-cache string     캐시된 저장소 색인이 포함된 파일의 경로 (기본값 "~/.cache/helm/repository")
      --repository-config string    저장소 이름 및 URL 을 포함하는 파일 경로 (기본값 "~/.config/helm/repositories.yaml")
```

### 함께 보기

* [helm dependency](helm_dependency.md)	 - 차트의 종속성을 관리

###### Auto generated by spf13/cobra on 29-Oct-2020
