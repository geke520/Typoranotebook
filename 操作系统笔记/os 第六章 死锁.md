### 第六章 死锁

#### 死锁的基本概念

   多个进程因竞争资源而造成的一种僵局，若无外力作用，这些进程将永远无法推进

#### 死锁产生的必要条件

   * 互斥

     在出现死锁的系统中，至少存在一个资源需要互斥使用，如果另一个进程需要，则必须等待该资源被释放。

   * 占有并等待

     一个进程必须占有至少一个资源并等待另一个资源，而该资源为其他进程所占有。

   * 非抢占

     资源不能被抢占，只能在进程完成之后自动释放

   * 循环等待

     有一组等待进程{P0,P1,P2,…,Pn}，其中Pi等待的资源被Pi+1占有(i=0,1,…,n-1)，Pn等待的资源被P0占有

#### 死锁预防方法——预先静态资源分配方法、有序资源使用方法

   * 破坏占有并等待

     * 方法一：每个进程执行之前必须申请并获得所需要的所有资源，后才能开始运行，在运行过程中进程只能释放资源不能申请资源
     * 方法二：进程提出申请资源前必须释放已占有的一切资源
     * 缺点：资源利用率很低，进程可能出现饥饿

   * 破坏非抢占

     * 方法一：当进程Pi申请Rj类资源时，检查Rj中有无可用资源：有则分配给Pi ；否则将Pi占有的资源全部释放而进入等待状态（Pi等待其原占有的所有资源和申请的资源）
     * 方法二：当进程Pi申请Rj类型的资源时检查Rj中有无可用资源：有则分配给Pi ；否则检查已获得Rj类资源的进程Pk，若Pk处于等待资源状态，则抢占Pk的Rj类资源并分配给Pi，若Pk不处于等待资源状态，则置Pi于等待资源状态（此时Pi原已占有的资源可能被抢占）

   * 破坏循环等待

     * 采用资源顺序分配法可以破坏循环等待条件：给系统中的所有资源编号，即寻找一个函数F: R→N（R：资源类型集合，N：自然数集合）
     * 进程只能按递增顺序申请资源，即进程申请类型为Ri的资源后，当且仅当F( Rj )> F( Ri )时，进程可以申请类型为Rj的资源
     * 如果进程需要同一资源类型的多个实例，则必须对它们一起进行申请
     * 当一个进程需要申请资源Rj时，必须先释放所有的资源Ri (F(Ri)≥ F(Rj ))

   * 破坏互斥

     临界资源的访问就必须是互斥进行

#### 死锁避免方法——安全状态和不安全状态、银行家算法

   * 系统安全/不安全状态

     * 进程序列< P1,P2,…, Pn >，如果对于每个Pi， Pi还需申请的资源数小于当前可用资源加上所有进程Pj (其中j<i) 所占有的资源，那么这一序列称为**安全序列**
     * 如果存在一个安全序列，那么系统则处于**安全状态**，否则就处于**不安全状态**
   * 避免死锁
   * 确保系统始终处于安全状态，当进程申请一个可用资源时，必须确保进行资源分配后，系统仍然处于安全状态，才能满足进程的申请

#### 死锁检测方法——资源分配图

   * 如果资源分配图没有环，那么系统中一定不存在进程死锁
   * 如果资源分配图中有环，则可能存在死锁
     * 当每种资源类型只有1个实例时，如果图中存在环，则一定有进程死锁→此时，环检测可用于检测死锁的存在

#### 死锁处理方法

   * 确保系统不会发生死锁

     * 死锁预防
     * 死锁避免

   * 无法确保系统不会发生死锁，提供处理机制

     * 死锁检测

     * 死锁恢复

   * 忽视死锁