# komodoAPI-cpp


```
sudo apt-get install libjsonrpccpp-dev libjsonrpccpp-tools

$ g++ komodoapi.cpp -o komodoapi -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client
/usr/lib/gcc/x86_64-linux-gnu/5/../../../x86_64-linux-gnu/crt1.o: In function `_start':
(.text+0x20): undefined reference to `main'
collect2: error: ld returned 1 exit status
```


Suggestion from slack:

bvbfan [2:17 AM]
It should be 
g++ komodoapi.cpp -o komodoapi -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client


Something like this:

 sudo apt-get install libjsoncppclient-dev libjsonrpccpp-dev
 g++ -o komodoapi -lcurl -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client komodoapi.cpp

Gets this sort of error output
 komodoapi.cpp:(.text+0xff80): undefined reference to` Json::Value::~Value()'

