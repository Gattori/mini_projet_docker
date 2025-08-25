from  python:3.11-slim
LABEL maintainer="Alex"
COPY requirements.txt  student_age.py /
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    python3-dev \
    libsasl2-dev \
    libldap2-dev \
    libssl-dev \
    gcc \
    && rm -rf /var/lib/apt/lists/*

RUN pip3 install -r /requirements.txt
volume ["/data"]
EXPOSE 5000
CMD ["python3", "/student_age.py"]
