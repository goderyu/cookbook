[Embind官方文档](https://emscripten.org/docs/porting/connecting_cpp_and_javascript/embind.html#embind)

```c++
// person.h 
struct Person { 
  std::string name;
  int age;
  Person(const std::string& name, int age) : name(name), age(age) {}
  void sayHello() {
    std::cout << "Hello, my name is " << name << " and I am " << age << " years old." << std::endl;
  } 
  // 重载函数
  void sayHello(const std::string& message) {
    std::cout << "Hello, " << message << std::endl;
  }
};
```

```c++
// person_binding.cpp
#include <emscripten/bind.h>
#include "person.h"
using namespace emscripten;
EMSCRIPTEN_BINDINGS(person) {
  class_<Person>("Person")
    .constructor<std::string&, int>()
    .property("name", &Person::name)
    .property("age", &Person::age)
    .function("sayHello", &Person::sayHello)
    .function("sayHello", pure_virtual(&Person::sayHello)); // 绑定重载函数
    // 如果有需要，可以在这里添加更多的绑定细节
}
```

