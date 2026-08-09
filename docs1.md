# docs1详情

## Task1

```go
// 2.go
fmt.Fscan(os.Stdin, &h) // 读取位置，地址
fmt.Scan(&h)            // 只需要地址，默认从 os.Stdin 读
```
* 两种方式都将空格/换行当做分隔符