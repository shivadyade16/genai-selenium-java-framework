# genai-selenium-java-framework

Production-ready Selenium + Java QA automation framework (sample).
- Maven, TestNG, SLF4J + Log4j2, Allure
- Page Object Model, RetryAnalyzer, TestListener (screenshots + stacktrace)
- Docker + docker-compose with selenium/standalone-chrome
- GitHub Actions and Jenkinsfile examples

## Quick commands

```bash
mvn -Dbase.url=https://demo-ecommerce.example -Dselenium.grid.url=http://localhost:4444 test

# build Docker test-runner
mvn -DskipTests clean package
docker build -t genai-tests -f docker/Dockerfile.test-runner .

docker-compose up --build

# generate Allure report
allure generate target/allure-results -o target/allure-report --clean
```
