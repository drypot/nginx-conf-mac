# Nginx Conf

개발용 맥에서 사용하는 nginx 설정.

## nginx.conf 세팅

    $ cd /usr/local/etc/nginx
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
