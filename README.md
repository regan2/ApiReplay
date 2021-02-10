# ApiReplay
replay api data from udl

### To Build
1. run `gradlew build`.  The built jar will be in ./build/libs

### To run
1. run `java -jar <jar filename> [arguments]`

#### Usage:
```
replay  -h hostAddress -d queryFileDirectory [-u username -p password] [-a authString] [-s playback_speed] [-?]
                                   hostAddress             the address of the Rest endpoints.
                                   queryFileDirectory      The directory that contains the json data to push to the api
                                   username,password       The username and password for authorization for the api endpoints
                                   authString              The encoded authstring for the authorization. Can be used in place
                                                               of the username/password pair
                                   playbackSpeed           The initial playback speed of the replayed data
                                   -?                      This usage message
                               
                                   Sample usage:
                                           java -jar replay.jar -h https://jsonplaceholder.typicode.com -d "./data/" -u fakeUser -p fakePassword
                                           java -jar replay.jar -h https://jsonplaceholder.typicode.com -d "./data/" -a "Basic bG9uZy51c2VybmFtZTpQQCQkdzBSZDEyMy4uNw==" -s 20

```
