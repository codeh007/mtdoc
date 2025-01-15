export HTTP_PROXY="http://127.0.0.1:10809" && export HTTPS_PROXY="http://127.0.0.1:10809"


## postgresql 释放连接
```sql
SELECT pg_terminate_backend(pid)
FROM pg_stat_activity
```


## go mod tidy设置
export GOPROXY=https://goproxy.cn,direct && export GO111MODULE=on

## git pull
```
#!/bin/bash

max_attempts=30
attempt=1
success=false

while [ $attempt -le $max_attempts ] && [ "$success" = false ]; do
    echo "Attempt $attempt of $max_attempts"
    if git pull; then
        echo "Git pull successful!"
        success=true
    else
        echo "Git pull failed, waiting 5 seconds before retry..."
        sleep 5
        ((attempt++))
    fi
done

if [ "$success" = false ]; then
    echo "Failed to git pull after $max_attempts attempts"
    exit 1
fi

```
