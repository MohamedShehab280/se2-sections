# Selenium project

Every piece of code from the sections, in one Maven project.

## What you need

- **Java** 11 or newer
- **IntelliJ IDEA** (Community is enough)
- **Google Chrome**

You do **not** need to download ChromeDriver or any `.jar` by hand. Maven downloads Selenium and
TestNG, and Selenium downloads the Chrome driver by itself the first time you run a test.

## Open it

1. IntelliJ › **File › Open** › choose `pom.xml` › **Open as Project**.
2. Wait for Maven to finish downloading (the progress bar at the bottom right). The first time needs internet.
3. Open `src/test/java/week3/FirstProject.java` and click the green ▶ next to the class name.

## Week 3

Two files, to show you the shape. The rest you write yourself in the lab sheet.

| File | What it shows |
|---|---|
| `FirstProject` | The shape of a test: `@Test`, open Chrome, go to a page, print the title, close. |
| `BrowserActions` | Every browser command from the section, each behind a method with a clear name: navigation, window size and position, page title and URL, tabs and handles, closing. It has no `@Test`, so it does not run on its own. Use it as a reference. |

## Your task before next week

Create a **new** Maven project yourself (do not just open this one), add the two dependencies to
`pom.xml`, reload Maven, and get `FirstProject` running. Then do Part B of the
[lab sheet](../week-03/Week%203%20-%20Lab%20Sheet.pdf) in that project.

```xml
<dependencies>
    <dependency>
        <groupId>org.seleniumhq.selenium</groupId>
        <artifactId>selenium-java</artifactId>
        <version>4.43.0</version>
    </dependency>
    <dependency>
        <groupId>org.testng</groupId>
        <artifactId>testng</artifactId>
        <version>7.12.0</version>
    </dependency>
</dependencies>
```

## If something does not work

| Problem | Fix |
|---|---|
| Red `Cannot resolve symbol` everywhere | Maven is still downloading. Wait, or right-click `pom.xml` › **Maven › Reload project**. |
| `SessionNotCreatedException` | Chrome is not installed, or this is the first run and there is no internet to download the driver. |
| The `java` folder under `test` is not green | Right-click it › **Mark Directory as › Test Sources Root**. |
