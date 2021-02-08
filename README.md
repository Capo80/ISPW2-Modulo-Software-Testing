# ISPW2-Modulo-Software-Testing
Repository di consegna per il modulo software testing di ISPW2.

Per fare la build eseguendo solamente i test sviluppati per il corso usare i comandi:

```
mvn '-Dtest=org.apache.zookeeper.mytests.*Test' -DfailIfNoTests=false clean verify
mvn '-Dtest=org.apache.bookkeeper.mytests.*Test' -DfailIfNoTests=false clean verify
```

Questi comandi genereranno anche i report di jacoco, per generare quelli di pit usare i comandi:

```
mvn org.pitest:pitest-maven:mutationCoverage surefire:test '-Dtest=org.apache.zookeeper.mytests.*Test' -DfailIfNoTests=false 
mvn org.pitest:pitest-maven:mutationCoverage surefire:test '-Dtest=org.apache.bookkeeper.mytests.*Test' -DfailIfNoTests=false 
```

La generazione dei report di pit sul mio computer è stata particolarmente lenta quindi ho incluso nella repository due zip contenenti dei report già calcolati.

## Links

BOOKKEEPER GitHub: https://github.com/Capo80/bookkeeper
BOOKKEEPER TravisCI: https://travis-ci.com/github/Capo80/bookkeeper
BOOKKEEPER SonarCloud: https://sonarcloud.io/dashboard?id=Capo80_bookkeeper

ZOOKEEPER Github: https://github.com/Capo80/zookeeper_testing
ZOOKEEPER TravisCI: https://travis-ci.com/github/Capo80/zookeeper_testing
ZOOKEEPER SonarCloud: https://sonarcloud.io/dashboard?id=Capo80_zookeeper_testing

