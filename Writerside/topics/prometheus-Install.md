# Install

## Prometheus 설치

1.  prometheus 공식 문서 페이지에서 원하는 버전으로 다운로드 후, 압축해제합니다.  
```Bash
cd /tmp
curl -LO "https://github.com/prometheus/prometheus/releases/download/v2.53.2/prometheus-2.53.2.linux-amd64.tar.gz"
tar -zxvf prometheus-2.53.2.linux-amd64.tar.gz
mv prometheus-2.53.2.linux-amd64 /etc/prometheus
mv /etc/prometheus/prometheus /usr/bin
mv /etc/prometheus/prometool /usr/bin
mkdir /prometheus   # prometheus data directory
```

2. 서비스 파일을 생성한다.  

파일 : /etc/systemd/system/prometheus.service
```text
[Unit]
Description=Prometheus

[Service]
ExecStart=/usr/bin/prometheus \
          --config.file="/etc/prometheus/prometheus.yml" \
          --storage.tsdb.path="/prometheus" \
          --enable-feature=remote-write-receiver \
          --web.enable-lifecycle \
          --storage.tsdb.max-block-duration=2h \
          --storage.tsdb.min-block-duration=2h \
          --web.enable-admin-api

ExecReload=/bin/kill -HUP $MAINPID

[Install]
WantedBy=multi-user.target
Alias=prometheus.service
```

## 파일 설명
파일을 압축해제하면 기본적으로 다음과 같은 파일이 생긴다.

![prometheus-ls.png](prometheus-ls.png)

| 파일 명              | 설명                                            |
|-------------------|-----------------------------------------------|
| LICENSE           | Prometheus의 라이센스에 대한 정보가 들어있다.                |
| NOTICE            | code들의 라이센스 정보가 들어있다.                         |
| console_libraries | Prometheus WebUI를 사용할 때, 라이브러리(페이지 목록) 파일들이다. |
| consoles          | Prometheus WebUI를 사용할 때, 대시보드(페이지) 파일들이다.     |
| prometheus        | prometheus 실행파일이다.                            |
| prometheus.yml    | prometheus 설정파일이다.                            |
| promtool          | prometheus 관리를 위한 도구이다.                       |