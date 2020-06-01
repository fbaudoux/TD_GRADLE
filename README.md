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

```
task myTask {
    ext.myProperty = "myValue"
}

task printTaskProperties {
    doLast {
        println myTask.myProperty
    }
}
```

création de méthodes 
```
task loadfile {
    doLast {
        fileList('./mydirectory').each { File file ->
            println "I found  $file.name"
        }
    }
}

File[] fileList(String dir) {
    file(dir).listFiles({file -> file.isFile() } as FileFilter).sort()
}
```
