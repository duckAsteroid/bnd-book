# 32 Maven Plugin



![][1]



# 32 Maven

The Maven plugin is described at [Felix maven plugin][2]. Defaults for Maven are: 



    Bundle-SymbolicName: <groupId>.<artifactId>
     Bundle-Name:         project.getName();
     Bundle-Version:      <version>
     Import-Package:      *
     Export-Package:      <groupId>.<artifactId>.* (unless Private-package is set)
     Bundle-Description:  project.getDescription()
     Bundle-License:      project.getLicenses())
     Bundle-Vendor:       project.getOrganization();
     Include-Resource:    src/main/resources
    

The repository with the latest plugin is: 



    <http://repo1.maven.org/maven2>
    
      Group ID: org.apache.felix
      Artifact: maven-bundle-plugin
    

Other details are found at the Felix site, the plugin is independently maintained by Felix.

 [1]: http://www.aqute.biz/uploads/Code/bnd.png ""
 [2]: http://felix.apache.org/site/apache-felix-maven-bundle-plugin-bnd.html