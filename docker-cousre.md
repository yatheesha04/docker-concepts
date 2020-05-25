1.	Before cloud , problems of hosting website are

  a.	Buy server
  
  b.	If traffic is in peeks, buy more servers
  
  c.	Monitoring and maintenance of server
  
  d.	Setup is expensive
  
  e.	Troubleshooting problem takes more time than business goals
  
  f.	Snice traffic is varing , some of  servers will be idele most of the time
  
  
  
  ----------------------------------------------
  Docker    https://www.youtube.com/watch?v=Rt5G5Gj7RP0&feature=youtu.be


  1.	https://www.youtube.com/watch?v=Rt5G5Gj7RP0&feature=youtu.be
  2.	To creare jar :maven build->goal as package
  3.	To run jar : go to project director till target folder and use this cmd
  
	  java -jar target\docker-in-5-steps-todo-rest-api-h2-1.0.0.RELEASE.jar
    
  4.	https://www.simplilearn.com/docker-tutorial-article
  5.	To run jar we need some prerequits like jdk, etc
  6.	To make it easy, use container  which contains jar along with softwares required to run jar. This makes easy to run jar on other systems than vm(virtual machines)
  7.	Manually create a new docker image
  
    a.	https://github.com/in28minutes/docker
  
  8.	Openjdk:8 is image  used to run java application(base image)
  
     a.	docker run -dit openjdk:8-jdk-alpine 
     
        i.	get image from docker remote reposity and run container

  9.	copy application jar to openjdk container using cmd
  
    a.	docker container cp target/docker-in-5-steps-todo-rest-api-h2-1.0.0.RELEASE.jar containername/id :/tmp
    
  10.	to check,list all files in tmp  using cmd
  
    a.	docker container exec containername/id ls /tmp
    
  11.	create new image (here base image in openjdk, we are using openjdk container with jarfile added into it)
  
      a.	docker container commit basecontainer imagename(to be created):v1
      
   12.	to run jar on this image
   
      a.	docker container commit --change='CMD ["java","-jar","/tmp/docker-in-5-steps-todo-rest-api-h2-1.0.0.RELEASE.jar"]'  vibrant_jones firstimage:v2
      b.	


