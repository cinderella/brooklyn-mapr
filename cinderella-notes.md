


## Configuration ##

Add the following to `~/.brooklyn/brooklyn.properties`:

```
# mapr-cinderella

brooklyn.location.named.cinderella-ec2=jclouds:ec2:http://localhost:8080/api/
brooklyn.location.named.cinderella-ec2.identity=YOUR_CINDERELLA_ACCESS_KEY
brooklyn.location.named.cinderella-ec2.credential=YOUR_CINDERELLA_SECRET_KEY
brooklyn.location.named.cinderella-ec2.imageId=Cluster01-Cloudsoft/ami-28f613b28f64497c93c4a78c4f2a4c29
brooklyn.location.named.cinderella-ec2.user=root

brooklyn.jclouds.ec2.identity=YOUR_CINDERELLA_ACCESS_KEY
brooklyn.jclouds.ec2.credential=YOUR_CINDERELLA_SECRET_KEY
```

## Build ##

From `brooklyn-mapr`, run `mvn clean install`


## Run ##

1. Start Cinderella instance
2. From cmd line: `brooklyn launch -a io.cloudsoft.mapr.MyM3App -l named:cinderella-ec2`