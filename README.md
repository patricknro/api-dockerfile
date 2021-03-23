# Projeto API usando Dockerfile

### Link tutorial
- https://docs.microsoft.com/en-us/visualstudio/containers/container-tools?view=vs-2019 <br /><br />
- https://www.alura.com.br/artigos/desvendando-o-dockerfile?gclid=CjwKCAjwgOGCBhAlEiwA7FUXkixYsQdglQfbrTvV8a1kUiIaL4HsSDO3pjNA9ji9_xorQaVs__aVlxoCS00QAvD_BwE

### Sobre o Dockerfile
**FROM** - Imagem <br />
**RUN** - Comando do terminal, podendo haver vários que não será sobrescrito. <br />
**CMD** - Comando no terminal, pode haver vários mas o último sobrescreve os anterios e também é executado. <br />
**ENTRYPOINT** - Faz a mesma coisa que o CMD, porém não pode ser sobrescrito. <br />
**ADD** - Copia arquivos ou diretórios para dentro da imagem docker, além disso pode fazer donwload de uma URL e até mesmo descompactar arquivos para o diretório de destino na imagem. <br />
**COPY** - Copia apenas diretórios ou arquivos. <br />
**EXPOSE** - Não publica porta, mas faz uma comunicação entre quem escreveu o Dockerfile e quem executará o container, servindo apenas como documentação. <br />
**VOLUME** - Cria uma pasta em nosso container que será compartilhada entre o container e o host. <br />
**WORKDIR** - Definir o diretório de trabalho quando o container estiver em execução. <br />

### cURL
```
curl --location --request GET 'http://localhost:32769/api/values/'
```

