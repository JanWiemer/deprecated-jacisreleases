# jacisreleases
Maven Repository containing JACIS releases
An exampe gradle to use JACIS can look as folloes:

<pre>
apply plugin: 'java'
apply plugin: 'maven'

sourceCompatibility = 1.8
version = '1.0'
group = 'org.jacisclientexample'

jar {
    manifest {
        attributes 'Implementation-Title': 'Jacis Client Example',
                   'Implementation-Version': 1.0,
                   'Implementation-Vendor' : "Jan Wiemer"
     }
 }
repositories {
    mavenCentral()
     maven {
        url 'https://github.com/JanWiemer/jacisreleases/raw/master/maven-repository/'
    }
}
dependencies {
    compile group: 'org.jacis', name: 'jacis', version: '1.0'
}
</pre>
