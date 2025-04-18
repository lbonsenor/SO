Blocked -> Running: `NO SE PUEDE`: Solo el scheduler elige quien corre y el mismo solo elige ready
Running -> Blocked: Process blocks for input
Blocked -> Ready: Input becomes available
Ready -> Blocked: `NO SE PUEDE`: Se bloquea por la ejecucion de una syscall, que solo pasa en running
Ready -> Running: Scheduler picks this process
Running -> Ready: Scheduler picks another process
