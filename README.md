# ThreadHW

## 使用 Callable 計算費氏數列
題目：
請實作一個 Callable<Integer> 類別，計算費氏數列的第 n 個數字，並透過 ExecutorService 提交該任務，最後取得並印出結果。

條件：
- 使用 Callable<Integer> 來計算費氏數列 (fib(n) = fib(n-1) + fib(n-2))
- 使用 ExecutorService 來管理執行緒池
- 透過 Future<Integer> 取得運算結果

## 使用 FixedThreadPool 進行大量計算
題目：
假設你有 100 個數字，每個數字的計算需要花費 1 秒，請使用 FixedThreadPool 來加速這些計算，並統計總計算時間。

條件：
-  創建 FixedThreadPool，執行緒數為 10
-  使用 ExecutorService.submit() 來提交 100 個任務
-  計算總花費時間

## 使用 ScheduledThreadPool 來執行定期任務
題目：
請實作一個排程執行緒池，讓它每隔 2 秒輸出 "Task executed"，共執行 5 次後自動終止。

條件：
- 使用 ScheduledExecutorService
- 讓任務每 2 秒執行一次
- 5 次執行後關閉執行緒池


## 使用 shutdownNow() 來強制停止執行緒
題目：
請實作一個排程執行緒池，讓它每隔 2 秒輸出 "Task executed"，共執行 5 次後自動終止。

條件：
- 使用 ExecutorService 來啟動 3 個長時間運算的執行緒
- 讓每個執行緒執行 10 秒的 while 迴圈
- 在 5 秒後使用 shutdownNow() 來強制終止執行緒
- 捕捉 InterruptedException 來檢查是否成功終止

## 實作cancel task 來停止任務
題目：
請實作一個帶有cancel方法的runnable 裡面會一直印出數字 call cancelTask()後則可以終止任務

條件：
- 使用 ExecutorService 來啟動 1 個需要長時間執行的task
- 實作cancel方法 讓任務不要執行完就先中斷
