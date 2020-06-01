# TD_GRADLE 

WIP

```
task hello {
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

```
task hello {
    doLast {
        println 'Hello Earth'
    }
}
hello.doFirst {
    println 'Hello Venus'
}
hello.configure {
    doLast {
        println 'Hello Mars'
    }
}
hello.configure {
    doLast {
        println 'Hello Jupiter'
    }
}

```

```
> gradle -q hello
Hello Venus
Hello Earth
Hello Mars
Hello Jupiter
```

