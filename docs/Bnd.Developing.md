# 40 Developing with bnd



![][1]

TBD 



# 40 Developing with bnd

In general you find the interesting stuff in aQute.lib.osgi.*. Look at the test cases for how the API can be used. 



## Example Making a Bundle

    Builder b = new Builder();
      b.setProperty( EXPORT_PACKAGE, "org.osgi.framework" );
      b.addClasspath( new File("jar/osgi.jar") );
    
      Jar jar = b.build();
      Manifest m = jar.getManifest();
      jar.write( new File(b.getBsn()+".jar"));

 [1]: http://www.aqute.biz/uploads/Code/bnd.png ""