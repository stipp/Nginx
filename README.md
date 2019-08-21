# Nginx
Nginx configures

Файл конфигурации Nginx`а с разъяснениями 


user www-data; # указываем, от какого пользователя будет работать Nginx
worker_processes 4; # число рабочих процессов, рекомендуется ставить по количеству ядер
timer_resolution 100ms; # уменьшает число системных вызовов gettimeofday(), что приводит к увеличению производительности
worker_rlimit_nofile 8192; # заменяет ограничение на число используемых файлов RLIMIT_NOFILE дл¤ рабочего процесса.
worker_priority -5; # директива задает приоритет рабочих процессов от -20 до 20 (отрицательное число означает более высокий приоритет). 
pid /run/nginx.pid;
include /etc/nginx/modules-enabled/*.conf;  # подключаем конфиги из папки /etc/nginx/modules-enabled/




....
