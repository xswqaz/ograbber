# ograbber
* 올레티비 시간표를 xmltv형식으로 출력
* 재방송정보가 없기때문에 5일안에 녹화된 파일명을 grep하여 존재하면 재방송으로 간주
* 일주일에 2번이상 방송되는 프로그램에 미대응
* 채널정보는 스크립트안의 channel array를 편집

# 사용법
* 아래의 명령을 crontab에 추가하여 epg에 반영
* 1일치만 가져오기 때문에 1:00-1:30에 실행하는것이 좋습니다
~~~ 
ograbber | socat - UNIX-CONNECT:/path/to/sockfile 
~~~
