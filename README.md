# genai-selenium-java-framework

This repo provides a fully modular, production-ready Selenium + Java QA automation framework that:

Accepts user stories / acceptance criteria and generates full end-to-end tests (POM, locators, fixtures, test data).

Uses Maven, TestNG, SLF4J + Log4j2, Allure reporting, and supports parallel execution, retries, explicit waits, and flaky detection.

Integrates with CI/CD (GitHub Actions + Jenkins examples), builds Docker images, and executes tests inside Docker containers connected to a Selenium Grid (or standalone Chrome).

Produces traceable mapping: story → test cases → assertions (JSON/Markdown mapping file auto-generated per story)

Provides logs collection (file-based) and an optional ELK snippet (commented) for teams that want centralized logging.

Extension points for custom drivers, assertions, pages.
