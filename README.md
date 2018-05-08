# komodoAPI-cpp

Suggestion from slack:

bvbfan [2:17 AM]
It should be 
g++ komodoapi.cpp -o komodoapi -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client


Something like this:

 sudo apt-get install libjsoncppclient-dev libjsonrpccpp-dev
 g++ -o komodoapi -lcurl -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client komodoapi.cpp

Gets this sort of error output
 komodoapi.cpp:(.text+0xff80): undefined reference to` Json::Value::~Value()'

