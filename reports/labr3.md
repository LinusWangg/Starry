### 实验
根据strace busybox的syscall id与本系统ERROR下的syscall id进行返回值的对齐并修改，将原来的ENONET网络报错改成了ENOENT文件报错。rename的函数根据用新的文件覆盖前原先已有的代码进行修改即可，与队长一同完成。
### 问答
1. log库来源于cargo build过程中registry下载的路径的依赖库的src/lib.rs。
2. 忘记make clean会导致上一次生成的目标文件没有被清除，也会导致依赖库没有重新下载。
3. maturin执行testcases/judge的测试用例。
4. 在开头和结尾都输出可以看到该语句是否被执行完成，如果没有完成是在哪个函数中发生了错误。
5. sys_yield会让出cpu，所以只输出返回值无法对sys_yield下的程序进行追踪。
