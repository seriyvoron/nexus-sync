# nexus-sync
Sync between two sonatype nexus repositories
Until sonatype nexus 2, All maven artifact is just file and folder, so just copy or upload `storage` folder for sync to respositories
But nexus 3 stores artifact into DB. So only sync option is calling web API, sadly.
So I have made this script.
nexus 2
nexus 3

# Usage:
```groovy nexusSync.groovy [type] [sourceUrl] [toUrl]```

* type:      maven or npm
* sourceUrl: sync source. must end with '/'
* toUrl:     sync target. must end with '/'

# Example:
```groovy nexusSync.groovy maven http://localhost:8081/nexus/maven-public/ http://my-private-nexus.com/nexus/private_repository/```
