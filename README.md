# komodoAPI-cpp


```
sudo apt-get install libjsonrpccpp-dev libjsonrpccpp-tools

$ g++ -c komodoapi.cpp -o komodoapi -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client

```


##Suggestion from slack during troubleshooting

goldenman [11:49 AM]
If you just want to try compile, add `-c`

`g++ -c komodoapi.cpp -o komodoapi -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client`


bvbfan [2:17 AM]
It should be 
g++ komodoapi.cpp -o komodoapi -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client


Something like this:

 sudo apt-get install libjsoncppclient-dev libjsonrpccpp-dev
 g++ -o komodoapi -lcurl -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client komodoapi.cpp

Gets this sort of error output
 komodoapi.cpp:(.text+0xff80): undefined reference to` Json::Value::~Value()'

