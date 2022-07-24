# load-test

Performance comparison between [**Gin**](https://github.com/gin-gonic/gin), [**Chi**](https://github.com/go-chi/chi), [**echo**](https://github.com/labstack/echo), [**fiber**](https://github.com/gofiber/fiber) and [**iris**](https://github.com/kataras/iris) web frameworks and **net/http** library

[go-web-framework-stars](https://github.com/mingrammer/go-web-framework-stars)

### Hardware specifications
 - Mem: 7.73G
 - Swap: 2.00G
 - CPU op-mode(s):                  32-bit, 64-bit
 - Byte Order:                      Little Endian
 - Address sizes:                   39 bits physical, 48 bits virtual
 - CPU(s):                          4
 - On-line CPU(s) list:             0-3
 - Thread(s) per core:              1
 - Core(s) per socket:              4
 - Socket(s):                       1
 - Vendor ID:                       GenuineIntel
 - CPU family:                      6
 - Model:                           158
 - Model name:                      Intel(R) Core(TM) i5-7400 CPU @ 3.00GHz
 - Stepping:                        9
 - CPU MHz:                         3000.001
 - BogoMIPS:                        6000.00

<div align="center">

|web framework / library| worker|user|rps |rt ||user|rps |rt ||user|rps |rt |
|:---:|:-----:|:----:|:----:|:-:|:----:|:----:|:----:|:----:|:-:|:----:|:----:|:----:|
|chi   |   4   |1   |420 |5 ms  ||10   |770 |30 ms  ||20   |1100 |35 ms  |
|iris  |4     |1  | 460   |  4ms ||10 | 1100  |  20ms||20 | 1200  |  40ms| 
|gin   |   4   |1   |400 |6 ms  ||10  |740 |30 ms ||20  |870 |45 ms |
|echo   |   4   |1   |660 |2 ms  ||10  |2100|12 ms ||20  |2200|17 ms |
|fiber   |   4   |1   |650 |3 ms  ||10  |2200|10 ms ||20  |2250|18 ms |  
|net/http   |   4   |1   |630 |2 ms  ||10  |1800|13 ms ||20  |2100|17 ms |

</div>

and the result of the load test taken on [Fast API](https://github.com/tiangolo/fastapi). In the same situation as Go web frameworks. The API was the GET method and returned only a simple Json

<div align="center">

|web framework| worker|user|rps |rt ||user|rps |rt ||user|rps |rt |
|:---:|:-----:|:----:|:----:|:-:|:----:|:----:|:----:|:----:|:-:|:----:|:----:|:----:|
|fastapi   |   4   |1   |310 |7 ms  ||10  |480 |33 ms ||20  |505|60 ms | 

</div>

## LICENSE
[GNU](https://github.com/lampesm/load-test/blob/main/LICENSE)
