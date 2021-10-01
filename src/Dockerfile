FROM python:3.8
WORKDIR /app
COPY requirements.txt . 
RUN python -m pip install -r requirements.txt
COPY . .
EXPOSE 5000
CMD ["gunicorn","--workers=3","--bind","0.0.0.0:5000", "app:app"]



# CRIAR IMAGEM 
# docker build -t flpmarcos/rotten-potatoes:v1 .

# LISTAR IMAGEM CRIADA
# docker image ls

# SUBIR A IMAGEM
# docker login
# docker push flpmarcos/rotten-potatoes:v1

# SUBIR LATEST DA IMAGEM (Boas praticas)
# docker tag flpmarcos/rotten-potatoes:v1 docker push flpmarcos/rotten-potatoes:latest
# docker push flpmarcos/rotten-potatoes:latest