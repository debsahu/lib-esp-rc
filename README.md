# ESP RC Library

### Usage

```c++

#include "esp_rc.h"

void setup() {

  EspRC.begin(1);
  
  EspRC.send("foo");
  EspRC.on("foo", [](){
    // Do somesimthing
  });

  EspRC.send("bar", "hello");
  EspRC.on("bar", [](String data){
    data.equals("hello");
  });
}

```