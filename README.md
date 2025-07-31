# Nginx Conf

개발용 맥에서 사용하는 nginx 설정.

## nginx 데몬으로 사용하지 않을 경우

    $ /opt/homebrew/bin/nginx -c $HOME/project/nginx-conf-mac/nginx.conf -g daemon\ off\;

## nginx 데몬으로 사용할 경우

기본 설정 폴더에 nginx.conf 세팅해 놓는다.

    $ cd /opt/homebrew/etc/nginx
    $ mv nginx.conf nginx.conf.org
    $ ln -s $HOME/project/nginx-conf-mac/nginx.conf .

    $ nginx -s reload 

## 사이트 활성화

abc 사이트를 활성화 할 수 있다.

    $ ln -s ../abc.conf sites/enabled
    $ nginx -s reload

## 기타

자세한 내용은 아래를 참고.

<https://github.com/drypot/web-memo>
