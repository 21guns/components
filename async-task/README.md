# async-task

```
class AsyncTsakParam {
    
}
interface AsyncTsakService {
    MessageResult run(AsyncTsakParam)
    
    MessageResult runDelay(AsyncTsakParam)
    
    void register(AsyncTsakListener)
}
/**
    执行异步任务
    1.异步线程
    2.MQ
*/
interface AsyncTsakEngine {
	
	/**
	    初始化执行引擎
	*/
	void init()
	/**
	    触发任务执行
	*/
	MessageResult trigger(AsyncTsakParam)
	/**
	    注册一个实际任务的执行器
	*/
	void register(AsyncTsakListener)
}
interface AsyncTsakListener {
	
	void execute(AsyncTsakParam)
}
class EmailAsyncTsakListner implements AsyncTsakListener{
	
}
/**
    使用示例
*/

```