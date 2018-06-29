# komodoAPI-cpp


```
sudo apt-get install libjsoncpp-dev libjsonrpccpp-dev libjsonrpccpp-tools

$ g++ -c komodoapi.cpp -o komodoapi -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client

```

Then the rest is just notes with not much formatting


# Notes

##Suggestion from slack during troubleshooting

goldenman [12:24 PM]
If you want to implement main on the other source file.
1. get object file of library `$ g++ -c komodoapi.cpp -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client`
2. you can see `komodoapi.o` file genrated.
3. generate `main.cpp` file
```
#include "komodoapi.h"

int main() {
        return 0;
}
```
4. `$ g++ -o komodotest main.cpp  komodoapi.o -ljsoncpp -ljsonrpccpp-common -ljsonrpccpp-client`
5. `$ ./komodotest`

Thanks for the tip, lol

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

