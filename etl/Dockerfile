# Укажите необходимую версию python
FROM python:3.10

# Выберите папку, в которой будут размещаться файлы проекта внутри контейнера
WORKDIR /opt/etl

# Заведите необходимые переменные окружения
ENV ALLOWED_HOSTS ['127.0.0.1']

# Скопируйте в контейнер файлы, которые редко меняются
COPY requirements.txt requirements.txt

# Установите зависимости
RUN pip install --upgrade pip && pip install -r requirements.txt


# Скопируйте всё оставшееся. Для ускорения сборки образа эту команду стоит разместить ближе к концу файла.
COPY . .


CMD python main.py