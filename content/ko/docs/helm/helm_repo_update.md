---
title: "Helm Repo Update"
---

## helm repo update

차트 저장소에서 로컬로 사용 가능한 차트의 정보를 업데이트한다.

### 개요


업데이트 명령어는 각 차트 레포지터리에서 차트에 대한 최신 정보를 가져온다. 
정보는 'helm search' 와 같은 명령에서 사용되는 것과 같이 로컬에 캐싱된다.


```
helm repo update [flags]
```

### 옵션

```
  -h, --help   helm repo update 명령어에 대한 도움말
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

* [helm repo](helm_repo.md)	 - 차트 저장소 추가, 나열, 제거, 업데이트, 색인 생성

###### Auto generated by spf13/cobra on 29-Oct-2020
