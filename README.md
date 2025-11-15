# hw5
1) Priority Inversion  and Priority Inheritance
   Q1) Priority inversion scenario
T1 - high priority -1
T3 - medium priority-2
T2 - low priority-3
   they are protected by a lock, only t1 and t2 need the lock
   At t = 0 , the low priority T2 arrives first, cpu is running t2 and enters the critical section.
   At t = 1 , T1 arrives and takes over the lock but t2 is holding the lock. Cpu is still running t2
   At t = 2 , T3 arrivse, since t3 does not need the lock it runs, takes over t2.
   This is priority inversion because despite t1 being higher priority, it is blocked because t2 is holding the lock.


   Q2) A)It takes 5 units of time to execute each protocol
   B) They complete at the same time
   C) It takes 12 units, both finish at the same time
   D) In protocol PIP
  E) Neither protocol allows t3 to take over t2.


2) Virtual and physical Addresses
   32 bit Os , 4kb, 1gb ram
    IA) 32 bit os is the virtual Address so it's 32 bits
   IB) 1 gb ram = 2^30 bytes = 30 bits
   IC) OS bit - offset = 20 Bits
   ID) Physical Page number = 30 - 12 = 18 bits
    IE) Page size = 4kb = 2^12= 4096 = 12 bits

   32 bit OS , 16kb,2gb ram
   IIA) 32 bits
   IIB) 2gb ram = 2^31 bytes = 31 bits
   IIC) Offset = log2(16384) = 14 bits, 31-14 = 18 bits
   IID) 31 - 14 = 17 bits
   IIE) 16kb = 2^14 = 14 bits

   64 bit Os, 16kb , 16gb ram

   IIA) 64 bits
   IIB) 16 * 2^30 = 2^34 = 34 bits
   IIC) Offset = 2^14 = 14 bits => 64 - 14 = 50 bits
   IID) 34 - 14 = 20 bits
   IIE 2^14 = 14 bits

   Sources
   https://documentation.ubuntu.com/real-time/latest/explanation/priority-inversion-inheritance/
   https://learn.microsoft.com/en-us/windows/win32/procthread/priority-inversion
   https://www.digikey.com/en/maker/projects/introduction-to-rtos-solution-to-part-11-priority-inversion/abf4b8f7cd4a4c70bece35678d178321
