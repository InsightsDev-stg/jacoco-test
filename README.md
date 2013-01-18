jacoco-test
===========

Sample project for the jacoco maven plugin:
* jacoco:prepare-agent is called several times.
* How often is phase `initialize` invoked when running `mvn clean verify site`?
* The `pom` as seen in https://github.com/mfriedenhagen/jacoco-test/blob/jacoco-prepare-agent-called-twice/pom.xml invokes `initialize` twice, because `maven-surefire-report-plugin:report` creates a forked lifecycle!
* One workaround is to define a `reportSet` for `maven-surefire-report-plugin` which uses goal `report-only` instead of `report`, see: https://github.com/mfriedenhagen/jacoco-test/blob/39939514cb2d8ac57bdd96500275ea31da875331/pom.xml#L78
