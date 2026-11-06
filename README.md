# kikitori-sources

Kikitori 컨테이너 이미지(`ghcr.io/logicool-tech/kikitori`)에 든 오픈소스 부품의 소스를 요청하는 곳이다. 코드는 이 저장소에 없다.

## 1. 이미지에 든 데비안 소스 패키지 목록

이미지 안 `/app/licenses/debian-sources.txt`에 있다. 앱을 띄우면 `http://<주소>:<포트>/licenses/debian-sources.txt`로도 열린다.
한 줄에 `<소스 패키지 이름> <판>` 하나다. 판은 이미지를 빌드할 때마다 바뀔 수 있으니 받은 이미지의 파일을 본다.

## 2. 데비안 소스 받는 곳

데비안은 판마다 소스를 보관한다. 주소 규칙:

```
https://snapshot.debian.org/package/<이름>/<판>/
```

예: `ffmpeg 7:7.1.5-0+deb13u1` → `https://snapshot.debian.org/package/ffmpeg/7:7.1.5-0+deb13u1/`

## 3. 요청하기

이 저장소에 이슈를 연다. 이미지 태그(예: `1.65.0`)나 digest와 받고 싶은 패키지 이름을 적는다.
이미지를 배포하는 동안과 마지막 배포 뒤 3년 동안, 요청하면 그 판 소스를 준다.
