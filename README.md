# iconland
基于cpp的icon编程语言思想

node
### 关键词
function 🆚 -->>
if 🆚 ?
else if  🆚 ?!
else 🆚 !
return 🆚 <<--
case 🆚 ->
console.log 🆚 log




日志：
📘
📗
📙
📕



### 例如：ex.il
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

// ✨ 是主入口
-->> main:
    getHello()
    💤1000     // 睡眠1s
    doFor()

```
