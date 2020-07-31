FROM  python:stretch

COPY . /app
WORKDIR /app

RUN pip3 install --upgrade pip
RUN pip3 install -r requirements.txt

EXPOSE 80

# RUN echo $(pwd)
# RUN echo $(gunicorn -v)
ENTRYPOINT ["gunicorn", "-b", ":8001", "main:APP"]