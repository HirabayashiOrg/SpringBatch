# リスナー
各処理の前後に処理をさせる、スキップ時にログを出力するといったことが可能になる

## 各処理ごとのリスナー
### Step
StepExecutionListner
```
@BeforeStep
@AfterStep
```
### Chunk
ChunkListener
```
@BeforeChunk
@AfterChunk
```
### ItemReader
ItemReadListener
```
@BeforeRead
@AfterRead
@OnReadError
```
### ItemProcessor
ItemProcessListener
```
@BeforeProcess
@AfterProcess
@OnProcessError
```
### ItemWriter
ItemWriteListener
```
@BeforeWrite
@AfterWrite
@OnWriteError
```
### Skip
SkipListener
```
@OnSkipInRead
@OnSkipInWrite
@OnSkipInProcess
```
> 対象のメソッドはアイテム単位で呼び出される  
> メソッドの呼び出しタイミングはコミットの直前  
> →　例外処理等でロールバックが走るとSkipListenerは効果ないよ  
