## SNAPHOT Voting_Async

## config.py


```
TIME - Время между запросами 1 адреса
TIMEMAX - рандомезирует время от 1 до TIMEMAX, что бы добавить чутка рандома между разными аккаунтами 
```

## data.txt
Пробегаетеь по всем proposal и собираете информацию

```
space@proposal@choise
space@proposal@choise
```

## proxy.txt

Прокси в формате:
```
username:password@ip:port
username:password@ip:port
```
Если используете один прокси на все акк продублируйте его что бы прокси было >= key

## key.txt

Вставлеяете свои приватные ключи

---------------------------------------------------------------------

Если появляется ошибка: (TypeError: Object of type bytes is not JSON serializable)
```
pip install web3==6.0.0b7 
pip install eth_account==0.7.0
```
