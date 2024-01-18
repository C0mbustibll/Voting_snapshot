## SNAPHOT Voting_Async

## config.py


```
TIME - Время между запросами 1 адреса
TIMEMAX - рандомезирует время от 1 до TIMEMAX, что бы добавить чутка рандома между разными аккаунтами 
TIME_ERROR - время ожидания после ошибки
PROXY - True/False в зависимости хотите ли использовать прокси
```

## data.txt
Пробегаетеь по всем proposal и собираете информацию

```
space@proposal@choise
space@proposal@choise

Пример как должен выглядеть proposal в файле data.txt для LayerZero по ссылке:

Ссылка - https://snapshot.org/#/stgdao.eth/proposal/0x747abdac9511413bf6bd752a9a5bbec93d07c68f57966429142eb26a92c09720
                                                 ||
                                                 \/
В файл data.txt - stgdao.eth@0x747abdac9511413bf6bd752a9a5bbec93d07c68f57966429142eb26a92c09720@1
```
![image](https://user-images.githubusercontent.com/117441696/212177066-ca0c2746-34d5-44ed-9ede-1efb85480e03.png)

Если в proposal можно выбрать > 1 голоса

Формат меняется на:
```
space@proposal@[choise]
space@proposal@[choise,choise]
```

![image](https://user-images.githubusercontent.com/117441696/227935482-243d8ec8-0d9a-4bd7-8080-982d5868e27a.png)
```
space@proposal@{"1":1}
space@proposal@{"CHOISE":NUM_VOTE}
```

## proxy.txt

Прокси в формате:
```
username:password@ip:port
username:password@ip:port
```
Если используете один прокси на все акк ,продублируйте его ,что бы прокси было >= key

## key.txt

Вставлеяете свои приватные ключи

---------------------------------------------------------------------

Если появляется ошибка: (TypeError: Object of type bytes is not JSON serializable)
```
pip install web3==6.0.0b7 
pip install eth_account==0.7.0
```
