# mogjdbc

## Stuff this uses

- [picocli4.3](https://github.com/remkop/picocli/tree/v4.3.0) included as source
- JDBC drivers in lib:
  - mysql-connector-java-8.0.20
  - postgresql-42.2.12
  - sqlite-jdbc-3.30.1

## Design goals

- No Ant/Gradle/Maven/etc. Minimal dependencies.
- Make it easier to use existing tests to test anything that speaks JDBC.
- Avoid complicated configuration or usage as much as possible, try to make things "just work".

## Notes

- Passwords are plaintext on the commandline and plaintext in memory. Strictly for development purposes.
- Developed against sqlite / postgresql / openjdk14.

## More things maybe

- Support an interactive record command to automatically generate JUnit tests.
- Figure out a way of getting individual tests to share data, without reinventing setup() / teardown().