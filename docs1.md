# docs1详情

## Task1

```go
// 2.go
fmt.Fscan(os.Stdin, &h) // 读取位置，地址
fmt.Scan(&h)            // 只需要地址，默认从 os.Stdin 读
```
* 两种方式都将空格/换行当做分隔符
---
```go
// 6.go
file,err:= os.Create("filename")
if err!=nil{

}
defer file.Close()
fmt.Fprintf(file,"str")
```
* defer 在错误检查后关闭文件，否则 Close nil 指针会 panic
* os.Create() 文件存在覆盖，不存在创建
---
切片和数组的区别

1. 切片可以自动扩容，数组长度在创建时就已经固定
2. 不同大小数组不兼容，属于不同类型
3. 切片可以通过数组初始化
4. 切片可以为空
5. 切片可以使用 len cap append copy 等函数
```go
// 切片创建方法
var s []int
s := []int
s := []int{...}
s := make([]int,len,cap)
s := arr[...]
s := s1[...]

// map创建方法
m := make(map[keytype]valuetype,cap)
m := map[string]int{
    "apple":1,
}
m := map[string]int{}   // 空 map 而不是 nil， 可以安全写入
var m map[string]int    // m==nil
```
---
