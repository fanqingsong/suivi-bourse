FROM python:3.12-slim

COPY requirements.txt /tmp/requirements.txt

RUN pip install --no-cache-dir -r /tmp/requirements.txt -i https://pypi.tuna.tsinghua.edu.cn/simple

RUN useradd --create-home appuser
WORKDIR /home/appuser
USER appuser

COPY ./src /home/appuser

EXPOSE 8081

ENTRYPOINT ["python3", "main.py"]
