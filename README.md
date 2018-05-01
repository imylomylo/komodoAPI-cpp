# komodoAPI-cpp

Something like this:

 sudo apt-get install libjsoncppclient-dev libjsonrpccpp-dev
 g++ -o komodoapi -lcurl -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client komodoapi.cpp

Gets this sort of error output
 komodoapi.cpp:(.text+0xff80): undefined reference to` Json::Value::~Value()'
