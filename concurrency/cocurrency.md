every core of cpu do their task and dont use whole of their power(capacity), they do their tasks and wait
we can use this wait time for doing another tasks, the core is unique and it is concurrency

in parallelism we have some cores and evey cores do defined tasks for us.|

wg is used when we have concurrent processes.
we define that for waiting until all processes be done.

go + func : it means we want to execute a function in a goroutine.

concurrency prevents CPU wastage.

The use of parallelism destroys the order of execution of tasks and any function that is executed sooner will announce its result sooner.

we can create a channel for example requests and connect many gorutines to it for reading and writing data.
gorutines listening to request and each goroutine process just a request, 
requests go to that goroutine that is not busy.
we define capacity for channel and say to it if you cant read or write data, never mind it, keep it in queue.

select is used for managing channels.

for example take the data in a channel then if it has no reader after 1 second, panic.
its very useful when our channel be full and we want to decide for data.
