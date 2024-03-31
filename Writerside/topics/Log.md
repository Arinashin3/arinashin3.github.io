# Logging

Prometheus는 기본적으로 tsdb를 이용하기 때문에 로그를 수집한 후에도 metric은 그대로 존재하게 된다.  
따라서 개인적으로는 로그 모니터링은 다른 솔루션을 이용하는 것을 권장한다.  

> Logging을 위한 exporter들  
log 모니터링을 위해 사용할 수 있는 exporter들은 아래와 같다.  
> ㅔasd

## Mtail
## grok exporter
grok exporter는 다음 2가지 방법으로 log alerts을 발생할 수 있다.  
일치하는 패턴이 존재 할때 alert 발생하는 방법과 로그 메세지를 alert 발생하는 방법 2가지가 존재한다.

<tabs>
    <tab title="패턴 감지">
        패턴 감지 Alert을 보내기 위해서는 다음과 같은 rule 1개로 설정할 수 있다.
        <code-block lang="plain text">![Alt Text](new_topic_options.png){ width=450 }</code-block>
    </tab>
    <tab title="로그 메세지">
        <code-block lang="xml">
            <![CDATA[<img src="new_topic_options.png" alt="Alt text" width="450px"/>]]></code-block>
    </tab>
</tabs>

## fluntd exporter(fluntd)asd
## telegraf



## node_exporter
## script_exporter