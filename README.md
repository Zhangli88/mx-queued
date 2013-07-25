<h1>mx-queued</h1>

The fast message queue server

-------------------------------------------------

使用协议:<br />
* 添加一个job到队列中:
<pre><code>
  <b>enqueue</b> &lt;queue_name&gt; &lt;priority_value&gt; &lt;delay_time&gt; &lt;job_size&gt;\r\n
  &lt;job_body&gt;\r\n
</code></pre>
queue_name: 队列的名称<br />
priority_value: job的优先值, 值越大越迟获取到<br />
delay_time: job要延时的秒数<br />
job_size: job的大小<br />
job_body: job的数据体<br />


* 从队列中获取一个job
<pre><code>
  <b>dequeue</b> &lt;queue_name&gt;\r\n
</code></pre>
queue_name: 队列的名称


* 获取队列的长度
<pre><code>
  <b>size</b> &lt;queue_name&gt;\r\n
</code></pre>
queue_name: 队列的名称


* 获取一个job, 并且把这个job暂时放置到回收站
<pre><code>
  <b>touch</b> &lt;queue_name&gt;\r\n
</code></pre>
queue_name: 队列的名称<br />

* 把回收站的指定ID的job放置到队列中
<pre><code>
  <b>recycle</b> &lt;recycle_id&gt; &lt;priority_value&gt; &lt;delay_time&gt;\r\n
</code></pre>
recycle_id: job在回收站的ID, 由fetch命令提供<br />
priority_value: job的优先值, 值越大越迟获取到<br />
delay_time: job要延时的秒数<br />

-------------------------------------------------

安装：
<pre><code>
$ cd mx-queue/
$ make
</code></pre>

-------------------------------------------------

联系QQ: 280259971<br />
新浪微博: @Yuk_松
