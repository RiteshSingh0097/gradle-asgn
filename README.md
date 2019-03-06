# gradle-asgn

1)
```
jar {
      manifest {
          attributes(
  
                  'Main-Class': 'Hello'
  
          )
      }
 }
```

2)
```
sourceSets {
    main {
        java {
            srcDirs = ['src/main/java', 'src/main/java2']
        }
        
    }
}
```


3) 
```
sourceSets {
    main {
        resources{
            srcDirs = ['src/main/resources']
            exclude 'file1.txt'
        }
    }
}
```

4)
```
repositories {
    mavenCentral()
}

dependencies {
    compile 'org.apache.commons:commons-lang3:3.8.1'
}

jar{
    from configurations.compile.collect{ zipTree it }
}

```




5)
```
repositories {
    jcenter()
}

```

6)
```
Apply from : ‘myTask.gradle’
```
