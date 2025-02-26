## MultiThreading:

```cpp
// Weather Forecast Application
/* Main Job of this project is to refresh the weather forecast data every two seconds*/

#include <iostream>
#include <string>
#include <thread>  // To Use Threads
#include <map>     // To Use Map Collection In Your Code
#include <chrono>
using namespace std::chrono_literals;   // Just to Use Milli Seconds In Our Code

void refreshForecast(std::map<std::string,int> forecastMap){
    while(true){
    for(auto& item : forecastMap){
        item.second++;
        std::cout << item.first<<" - "<< item.second << std::endl;     
    }
    std::this_thread::sleep_for(2000ms);

}}


int main(){

    std::map<std::string,int> forecastMap = {
        {"New York", 10},
        {"Detroit", 0},
        {"Chittoor", 35}  // Dummy data Created 
    };
    std::thread bgworker(refreshForecast, forecastMap);

    system("pause>nul");
}

```
