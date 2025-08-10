# Nginx Conf

개발용 맥에서 사용하는 nginx 설정.

## nginx.conf 연결

    $ cd /opt/homebrew/etc/nginx
    $ mv nginx.conf nginx.conf.org
    $ ln -s $HOME/project/nginx-conf-mac/nginx.conf .

## nginx 실행

nginx daemon 모드 끄고 실행.

    $ nginx -g "daemon off;"

nginx.conf 수정 후 테스트.

    $ nginx -t

nginx 데몬으로 돌고 있을 때, nginx.conf 리로딩.

    $ nginx -s reload 

## 사이트 추가

`/etc/hosts` 에 `***.test` 주소를 등록.

`sites/***.conf` 를 생성.

`sites/enalbed` 폴더로 심볼릭 링크를 생성.

    $ ln -s ../abc.conf sites/enabled

nginx 설정 테스트.

    $ nginx -t reload

nginx 설정 리로딩.

    $ nginx -s reload

## 기타

자세한 내용은 아래를 참고.

<https://github.com/drypot/web-memo>
