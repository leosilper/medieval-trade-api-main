# Usa uma imagem base do Java 17
FROM eclipse-temurin:17-jdk

# Diretório de trabalho dentro do container
WORKDIR /app

# Copia todos os arquivos do projeto para dentro do container
COPY . .

# Dá permissão de execução ao wrapper do Maven
RUN chmod +x mvnw

# Gera o JAR usando o Maven Wrapper, sem rodar os testes
RUN ./mvnw clean package -DskipTests

# Expõe a porta usada pela aplicação (Render define via variável PORT)
EXPOSE 8080

# Comando que roda a aplicação
CMD ["java", "-jar", "target/medieval-trade-api-0.0.1-SNAPSHOT.jar"]
