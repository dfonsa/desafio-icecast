# Use a imagem oficial do Nginx
FROM nginx:alpine

# Remova a configuração padrão do Nginx
RUN rm /etc/nginx/conf.d/default.conf

# Copie o arquivo de configuração personalizado para o diretório de configuração do Nginx
COPY nginx.conf /etc/nginx/conf.d/

# Exponha a porta 80 para acessar o Nginx
EXPOSE 80

# Comando de inicialização do Nginx
CMD ["nginx", "-g", "daemon off;"]

