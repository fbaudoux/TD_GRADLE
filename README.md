# TD_GRADLE 

WIP

```task hello {
doLast {
   println 'Hello world!'
  }
}
```

```
task hello {
    doLast {
        println 'Hello world!'
    }
}
task intro {
    dependsOn hello
    doLast {
        println "I'm Gradle"
    }
}
```

