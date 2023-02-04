# Change Java version with jenv

jenv: Manage Your Java Environment

jenv is a command line tool to help you forget how to set the `JAVA_HOME` variable.

GitHub: https://github.com/jenv/jenv

Check your java added to jenv

```bash
  jenv versions
```

![Img](https://res.cloudinary.com/dzwztfzvu/image/upload/v1675541317/Screen_Shot_2023-02-05_at_03.08.09_xaipos.png)

Use `jenv global VERSION` to set the global version of java

```bash
  jenv global 11.0
```

Then, check your java version

```bash
  java -version
```

![Img](https://res.cloudinary.com/dzwztfzvu/image/upload/v1675542503/Screen_Shot_2023-02-05_at_03.28.09_cacesl.png)
