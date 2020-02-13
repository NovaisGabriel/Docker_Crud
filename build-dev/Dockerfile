FROM python:3.7
LABEL maintainer 'Aluno Gabriel Novais'

RUN useradd www && \
    mkdir /app && \
    mkdir /log && \
    chown www /log

USER www 
VOLUME /log
WORKDIR /app
EXPOSE 8000

ENTRYPOINT ["/usr/bin/python3.7"]
CMD ["run.py"]