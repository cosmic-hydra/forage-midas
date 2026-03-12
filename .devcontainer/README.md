# GitHub Codespaces – forage-midas

This project is configured for GitHub Codespaces using a Java 17 devcontainer.

## Creating a Codespace

1. Go to the repository on GitHub.
2. Click the green **Code** button → **Codespaces** tab.
3. Click **Create codespace on flow** (the default branch for this repo).
4. Wait for the container to build and VS Code to open in the browser.

## Rebuilding the Container

If you change `.devcontainer/devcontainer.json` or need a clean environment:

1. Open the Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`).
2. Run **Codespaces: Rebuild Container** (or **Dev Containers: Rebuild and Reopen in Container**).

## Running / Building the Project

Once the Codespace is open, use the integrated terminal:

```bash
# Download dependencies (already run automatically on first open)
./mvnw dependency:resolve

# Compile the project
./mvnw compile

# Run all tests
./mvnw test

# Build a runnable JAR (skip tests for speed)
./mvnw -DskipTests package

# Run the application
./mvnw spring-boot:run
```

## Extensions Included

| Extension | Purpose |
|-----------|---------|
| `vscjava.vscode-java-pack` | Core Java support bundle |
| `redhat.java` | Java language server |
| `vscjava.vscode-maven` | Maven project explorer |
| `vscjava.vscode-java-debug` | Java debugger |
| `vscjava.vscode-java-test` | Java test runner |
| `nextdev.nextdev` | Nextdev agent |
