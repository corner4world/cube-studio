
FROM python:3.9

ENV TZ=Asia/Shanghai
ENV DEBIAN_FRONTEND=noninteractive
RUN pip config set global.index-url https://mirrors.aliyun.com/pypi/simple
RUN pip install kubernetes==25.3.0 pysnooper psutil requests huggingface_hub hf_transfer
RUN pip install modelscope
COPY job/model_download/ /app/

WORKDIR /app
ENV PYTHONPATH=/app:${PYTHONPATH:-}

ENTRYPOINT ["python3", "launcher.py"]


