jacoco-test
===========

Sample project for the jacoco maven plugin:
* jacoco:prepare-agent is called several times.
* How often is phase `initialize` invoked when running `mvn clean verify site`?
* The `pom` as seen in https://github.com/mfriedenhagen/jacoco-test/blob/jacoco-prepare-agent-called-twice/pom.xml invokes `initialize` twice, because `maven-surefire-report-plugin:report` creates a forked lifecycle!
