#c++�е��쳣����
## try..catch
���ǿ��Խ��� C++ �쳣����������������쳣�������������������쳣���﷨Ϊ��

```c++
try{
    // �����׳��쳣����� ���磺
    throw "Unknown Exception";  //�׳��쳣
}catch(exceptionType variable){
    // �����쳣�����
}
```
## �򵥵��쳣����
throw�׳�һ���쳣���ͣ�cathͨ���ж��Ƿ���Ϻ��߽�ȥ��

```c++
#include <iostream>
#include <exception>
using namespace std;
 
struct MyException : public exception
{
  const char * what () const throw ()
  {
    return "C++ Exception";
  }
};

int main()
{
  try
  {
    throw MyException();
  }
  catch(MyException& e)
  {
    std::cout << "MyException caught" << std::endl;
    std::cout << e.what() << std::endl;
  }
  catch(std::exception& e)
  {
    //�����Ĵ���
  }
}

```


## �����������쳣����
ͨ���ж϶�������;����׳��ĸ��쳣��
```c++
// exception constructor
#include <iostream>       // std::cout
#include <exception>      // std::exception

struct ooops : std::exception {
  const char* what() const noexcept {return "Ooops!\n";}
};

int main () {
  ooops e;
  std::exception* p = &e;
  try {
      throw e;       // throwing copy-constructs: ooops(e)
  } catch (std::exception& ex) {
      std::cout << ex.what();
  }
  try {
      throw *p;      // throwing copy-constructs: std::exception(*p)
  } catch (std::exception& ex) {
      std::cout << ex.what();
  }
  return 0;
}
```

## std::exception
��c++11�У�exception�౻����Ϊ

```c++
class exception {
public:
  exception () noexcept;
  exception (const exception&) noexcept;
  exception& operator= (const exception&) noexcept;
  virtual ~exception();
  virtual const char* what() const noexcept;
}
```
exceptions�д���һЩ�쳣�жϵĺ������������쳣����

![img](img/exceptions_in_cpp.png)
���庯��

![Alt text](img/image12.png)
[�����cplusplus](https://cplusplus.com/reference/exception/exception/)