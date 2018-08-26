
# JD Cloud C ++ Signature Library
## Basic Description
The JD Cloud C ++ signing tool provides the request signature function when C ++ language is used to access the JD Cloud OpenAPI.

Before apply for JD Cloud open API, [AccessKey management page](https://uc.jdcloud.com/accesskey/index) shall be called out for application of accesskey and secretKey Key Pair (AK/SK). AK/ SK information shall be kept properly and if lost, it is likely to cause illegal users to use this information to operate your resources on the cloud, resulting data or property losses.

This signature tool is available in a static library using the C++11 standard. The approximate process used is:
- Introducing the dependent header files and static libraries into your project through the cmake tool
- Fill in the HTTP request's information into the HttpRequest object of the signing tool
- Call signature interface
- Put the returned Authorization, x-jdcloud-date, x-jdcloud-nonce and its values into your real request Header
- Then initiate a call to JD Cloud OpenAPI gateway

## Linux（Ubuntu）
### Installation method
1) Installation and development dependency library
```
sudo apt-get install g++ cmake libssl-dev uuid-dev
```
2) Download the Demo instance from the GitHub, the address is: https://github.com/jdcloud-api/jdcloud-sdk-cpp-signer

### Application method
1) Project Catalogue of New Project
2) Write the cmake file, refer to the example in Demo, and reference the header file
```
include_directories(${PROJECT_SOURCE_DIR}/h)
include_directories(${PROJECT_SOURCE_DIR}/http)
include_directories(${PROJECT_SOURCE_DIR}/util)
include_directories(${PROJECT_SOURCE_DIR}/util/crypto)
include_directories(${PROJECT_SOURCE_DIR}/util/logging)
```
3) Reference static library
```
link_libraries(${PROJECT_SOURCE_DIR}/libjdcloudsigner.a)
link_libraries(ssl)
link_libraries(crypto)
link_libraries(uuid)
```
4) Refer to the main.cpp in Demo to call the signature interface. See section "call method" for details.
5) Compile link
```
cmake .
make
```

## macOS
### Installation method
1) Install the above version of cmake3.5
```
brew install cmake
```
2) Download the Demo instance from the GitHub, the address is: https://github.com/jdcloud-api/jdcloud-sdk-cpp-signer

### Application method
1) Project Catalogue of New Project
2) Write the cmake file, refer to the example in Demo, and reference the header file
```
include_directories(${PROJECT_SOURCE_DIR}/h)
include_directories(${PROJECT_SOURCE_DIR}/http)
include_directories(${PROJECT_SOURCE_DIR}/util)
include_directories(${PROJECT_SOURCE_DIR}/util/crypto)
include_directories(${PROJECT_SOURCE_DIR}/util/logging)
```
3) Reference static library (ssl library is brought with the mac system with no need to install)
```
link_libraries(${PROJECT_SOURCE_DIR}/libjdcloudsigner.a)
link_libraries(ssl)
link_libraries(crypto)
```
4) Refer to the main.cpp in Demo to call the signature interface. See section "call method" for details.
5) Compile link
```
cmake .
make
```
## Windows
### Installation method
1) The above version of Visual Studio 2015, the official address is: https://visualstudio.microsoft.com/
2) The above version of CMake 3.5, the official address is: https://cmake.org/
3) Download the Demo instance from the GitHub, the address is: https://github.com/jdcloud-api/jdcloud-sdk-cpp-signer

### Application method
1) Project Catalogue of New Project
2) Write the cmake file, refer to the example in Demo, and reference the header file
```
include_directories(${PROJECT_SOURCE_DIR}/h)
include_directories(${PROJECT_SOURCE_DIR}/http)
include_directories(${PROJECT_SOURCE_DIR}/util)
include_directories(${PROJECT_SOURCE_DIR}/util/crypto)
include_directories(${PROJECT_SOURCE_DIR}/util/logging)
```
3) Reference static library
```
link_libraries(${PROJECT_SOURCE_DIR}/jdcloudsigner.lib)
link_libraries(${PROJECT_SOURCE_DIR}/libeay32.lib)
```
4) Refer to the main.cpp in Demo to call the signature interface. See section "call method" for details.
5) Compile link

Open Visual Studio Developer Command Prompt, Execute
```
cmake .
devenv Demo.sln /build
```

Open the Demo.sln solution using Visual Studio, compile.

## Call method
```
// 引用头文件
#include "Credential.h"
#include "JdcloudSigner.h"
#include "http/HttpTypes.h"
#include "http/HttpRequest.h"
#include "util/logging/Logging.h"
#include "util/logging/ConsoleLogSystem.h"

// 配置日志
ConsoleLogSystem* cls = new ConsoleLogSystem(LogLevel::Debug);
shared_ptr<ConsoleLogSystem> log(cls);
InitializeLogging(log);

// 创建HttpRequest对象
HttpRequest request(URI("YOUR URL"), HttpMethod::HTTP_GET);
request.SetHeaderValue(CONTENT_TYPE_HEADER, "application/json");
request.SetHeaderValue(USER_AGENT_HEADER, "JdcloudSdkGo/1.0.2 vm/0.7.4");

// 创建签名对象
Credential credential("YOUR AK", "YOUR SK");
JdcloudSigner signer(credential, "vm", "cn-north-1");

// 调用签名方法
bool result = signer.SignRequest(request);
if(result)
{
    // 把Header中的三项 "Authorization、x-jdcloud-date、x-jdcloud-nonce" 放到真正的请求头中
    // 向京东云网关发起HTTP请求
}
else
{
    return;
}
```
