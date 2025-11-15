# OwenWilsonwow
api for owen-wilson-wow-api.onrender.com database wow saying by Owen Wilson in his movies.
# main
```cpp
#include "OwenWilsonwow.h"
#include <iostream>

int main() {
   OwenWilsonwow api;

    auto wow = api.random_wows(0,3).then([](json::value result) {
        std::cout << "Search results: " << result.serialize() << std::endl;
    });
    wow.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
