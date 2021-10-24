




# Strategy Steps



1.Source code checkout – Pull code from public GitHub repo

```
refer stage "Preparation" in jenkins file in root dir
```
2.Run Quality Checks using pre-build Docker Image & program.

```
Based on plugin configured for linting , we can run the command
refer stage "sonar stage"  as per my understanding we can run this by docker compose or kubernetes locally with mounted code by volume
```
3.Run UT using pre-build docker Image & program

```
refer build stage --Since code is mounted on volume, we can run our command into running container

```
4.Build Jar or python package using the docker image.

```
Once code meets all checks we can create new docker image from existing with added jars to be copied into latest image

```
5.Deploy the Jar or python to your local machine.

```
once jar is ready with new image we can launch new container with docker compose or kubernetes yaml
```
# Note:
1.There is no script prepared for copying data etc

```
```
2.All required stages are depicted here

```
```
3.Because of shortage of time high level concept is depicted

```
```
4.we can pickup all the required arguments from jenkins and same can be applied in script of for copying that too I also tried to depict

```

```
5.Linting can be done based on plug-in configured with java or python 

```

```