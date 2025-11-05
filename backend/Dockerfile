# =========================
# 1️⃣ Build Stage
# =========================
FROM eclipse-temurin:21-jdk AS build
WORKDIR /app

# Copy Maven files
COPY pom.xml .
COPY src ./src

# Package the application (skipping tests for faster build)
RUN ./mvnw clean package -DskipTests || mvn clean package -DskipTests

# =========================
# 2️⃣ Runtime Stage
# =========================
FROM eclipse-temurin:21-jre
WORKDIR /app

# Copy jar from build stage
COPY --from=build /app/target/*.jar app.jar

# Expose port (change if your app runs on a different one)
EXPOSE 8080

# Run the Spring Boot app
ENTRYPOINT ["java", "-jar", "app.jar"]

