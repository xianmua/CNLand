# iconland
设计一门类node但没有 `async` 和 `await` 的异步思想编程语言
草稿

### 关键词
function 🆚 -->> <br>
if 🆚 ? <br>
else if  🆚 ?! <br>
else 🆚 ! <br>
return 🆚 <<-- <br>
case 🆚 -> <br>
console.log 🆚 log <br>




日志：
📘
📗
📙
📕



### 例如：ex.cnl
```cpp

-->> doFor:
    loop ([1=>10], (i: number):
          ? (i > 3 && i < 6):
            log: "A等"
          ?! (i > 6 && i < 9):
            log: "B等"
          ! :
            log: "C等"
    )

///////生成的cpp代码///////////
/*
void doFor() {
    for(int i=0;i<10;i++) {
        if (i > 3 && i < 6) {
            std::cont << "A等";
        } else if (i > 6 && i < 9) {
            std::cont << "B等";
        } else {
            std::cont << "C等";
        }
    }
}
*/
//////////////////////

-->> getHello:
    msg := "Hello World"
    <<-- msg // return msg

-->> main:
    getHello()
    💤x1     // 睡眠1s
    doFor()

```
