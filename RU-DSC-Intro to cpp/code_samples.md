# Types

### Basic Types
```cpp
#include <iostream>

int main(){
  
  int a = 123;
  int b = 123.923;
  
  std::cout << "a = " << a << " b = " << b << std::endl;
  // a = 123 b = 123
  
  
  double c = 255.123;
  bool d = true;
  char e = 'e';
  std::cout << "c = " << c << " d = " << d << " e = "<< e << std::endl;
  // c = 255.123 d = 1 e = e
  
}
```
### Auto
```cpp
  auto a = 1123; // Deduced to an integer
  auto b = 123.123; // Deduced to a floating point number
  auto flag = true; // Deduced to a boolean
  auto c = 'c'; // Deduced to a char
```

### Strings
```cpp
#include <iostream>
#include <string>

int main (){
  
  std::string name = "Ahmad";
  
  std::cout << name << std::endl;
  // Ahmad
  
  std::cout << name.at(1) << std::endl;
  // h
  
  name.append(" Beirkdar");
  
  std::cout << name << std::endl;
  // Ahmad Beirkdar
 
}
```

# Containers:
### Vector
```cpp
std::vector<int> sample{1,2,3,4,5};
// sample -> [1,2,3,4,5]
sample.push_back(6);
// sample -> [1,2,3,4,5,6]
sample.at(1);
// 2
sample.at(1) = -9;
// sample -> [1,-9,3,4,5,6]

auto a = sample.at(-1);
// a = -9, type: int
```

### Array
```cpp
std::array<int, 3> sample{1, 2, 3};
// sample -> [1,2,3]
sample.at(1);
// 2
sample.at(0) = 99;
// sample -> [99,2,3]
```

# Control Flow
### Raw Loops
```cpp
std::vector<int> sample{1,2,3,4,5,6};
for(auto i = 0; i < sample.size(); i++){
  std::cout << sample.at(i);
}
// 123456
```
### Range Loops
```cpp
std::vector<int> sample{1,2,3,4,5,6};
for(int i : sample){
  std::cout << i;
}
// 123456
```
```cpp
std::vector<int> sample{1,2,3,4,5,6};
for(const auto& i : sample){
  std::cout << i;
}
// 123456
```

### Functions
```cpp
void fun1(int a){
  a += 3;
}

void fun2(int& a){
  a += 3;
}

int main(){
  int x = 9;
  
  fun1(x);
  std::cout << x << std::endl;
  // 9
  fun2(x);
  std::cout << x << std::endl;
  // 12
}
```