Commands used:
```
git clone git@github.com:uTensor/utensor-helloworld.git
cd utensor-helloworld/
rm uTensor.lib
mbed add https://github.com/sandeepmistry/utensor-arduino-demo
cd utensor-arduino-demo
git checkout arduino-library-structure
mbed sync
cd ..
mbed deploy
mbed new .
wget https://github.com/uTensor/uTensor/raw/develop/build_profile/release.json
```
-----------------------------
Build instruction:
```
import https://github.com/neil-tan/utensor_arduino_test
cd utensor_arduino_test
mbed compile -m auto -t GCC_ARM --profile=release.json -f
```
-----------------------------

Current errors:
```
...
Compile [  4.0%]: Ticker.cpp
Compile [  4.1%]: main.cpp
[Warning] utensor_string.hpp@13,34: comparison between signed and unsigned integer expressions [-Wsign-compare]
[Error] utensor_string.hpp@42,23: extra qualification not allowed [-fpermissive]
[Error] utensor_string.hpp@43,5: explicit specialization of non-template 'std::<anonymous struct>'
[Error] utensor_string.hpp@42,28: an anonymous struct cannot have function members
[Error] utensor_string.hpp@51,6: abstract declarator 'std::<anonymous struct>' used as declaration
[Error] hashtable_policy.h@85,34: no match for call to '(const std::hash<utensor::string>) (const utensor::string&)'
[Error] type_traits@154,38: 'value' is not a member of 'std::__and_<std::__is_fast_hash<std::hash<utensor::string> >, std::__detail::__is_noexcept_hash<utensor::string, std::hash<utensor::string> > >'
[Error] unordered_map.h@100,66: 'value' is not a member of 'std::__not_<std::__and_<std::__is_fast_hash<std::hash<utensor::string> >, std::__detail::__is_noexcept_hash<utensor::string, std::hash<utensor::string> > > >'
[Error] unordered_map.h@107,45: 'value' is not a member of 'std::__not_<std::__and_<std::__is_fast_hash<std::hash<utensor::string> >, std::__detail::__is_noexcept_hash<utensor::string, std::hash<utensor::string> > > >'
[Error] unordered_map.h@108,47: 'value' is not a member of 'std::__not_<std::__and_<std::__is_fast_hash<std::hash<utensor::string> >, std::__detail::__is_noexcept_hash<utensor::string, std::hash<utensor::string> > > >'
...
```