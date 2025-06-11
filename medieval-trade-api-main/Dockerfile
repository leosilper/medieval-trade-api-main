# Usa uma imagem base do Java 17
FROM eclipse-temurin:17-jdk

# Diretório de trabalho dentro do container
WORKDIR /app

# Copia os arquivos do projeto
COPY . .

# Gera o JAR com Maven Wrapper
RUN ./mvnw clean package -DskipTests

# Expõe a porta (será sobrescrita pela env PORT no Render)
EXPOSE 8080

# Comando de execução
CMD ["java", "-jar", "target/medieval-trade-api-0.0.1-SNAPSHOT.jar"]
