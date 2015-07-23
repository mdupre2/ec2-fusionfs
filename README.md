#ec2-fusionfs

##Description

Some useful scripts for running fusionfs on ec2

* `ec2-ip`: Retreives the list of public ip addresses of all running ec2 instances and stores them in `public_ip.txt`. Retreives the list of private ip addresses of all running ec2 instances and stores them in `private_ip.txt`

```
     Usage: ec2-ip
```

*  `ec2-start-service` : runs the start_service.sh script on all instances
```
     Usage: ec2-start-service
```

*  `ec2-start` : runs the start.sh script on all instances
```
     Usage: ec2-start
```

*  `ec2-stop-service` : runs the stop_service.sh script on all instances
```
     Usage: ec2-stop-service
```

*  `ec2-stop` : runs the stop.sh script on all instances
```
     Usage: ec2-stop
```

* `ec2-push` : push a file on local machine to all ec2 instances
```
     Usage: ec2-push  local_sorce_file insance_target_file
```

* `ec2-pull` : pulls files from all ec2 instances and stores in local directory
```
     Usage: ec2-pull  insance_source_file local_target_directory
``` 

* `ec2-mkdir` : makes directory on all ec2 instances
```
Usage: ec2-mkdir insance_new_directory
``` 

* `ec2-rm` : remove file on all ec2 instances
```
Usage: ec2-rm insance_file
``` 

##Setup
1. Create ec2 instances. All insances must have FusionFS installed in the same location. Having all the instances look the same is helpful. 
2. Fill in `ec2-config` file. Note that any environment variables exported in ~/.bashrc of the instance will not be exported. Export all environment variables in ~/.bash_profile. 
3. If you don't have a AWS user with **administative permissions**, [create a user](http://docs.aws.amazon.com/IAM/latest/UserGuide/ManagingCredentials.html). 
4. Use the downloaded credentials to fill in `AWS_ACCESS_KEY` and `WS_SECRET_KEY` in `ec2-config`

##Use
1. When ever you run new instances or stop an instance, call ec2-ip
2. Now you can use any of the scripts.
 


