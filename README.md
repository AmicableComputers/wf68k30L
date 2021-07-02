 # WF68K30L IP Core.

This is the top level structural design unit of the 68K30L complex instruction set (CISC) microcontroller. It's programming model is (hopefully) fully compatible with Motorola's MC68030. This core features a pipelined architecture. In comparision to the fully featured 68K30 the core has no MMU, no data and instruction cache and no coprocessor interface. This results in missing burstmodes which are not required due to lack of cache. Missing coprocessor operations are: cpBcc, cpDBcc, cpGEN, cpRESTORE, cpSAVE, cpScc, cpTRAPcc.  Missing MMU operations are: PFLUSH, PLOAD, PMOVE and PTEST.  The trap handler does not process the following exceptions which lack due to the missing MMU and coprocessor interface: PRE_EXC_CP, MID_EXC_CP, POST_EXC_CP, EXC_VECT_CP, MMU_CFG_ERR.  The shifter in the 68K30 is a barrel shifter and in this core it is a conventional shift register controlled logic.  This core features the loop operation mode of the 68010 to deal with DBcc loops. This feature is a predecessor to the MC68020/30/40 caches.  The exception handler works for the RTE but without taking the SSW into account which is intended to restore from a defectice bus error stack frame.

Enjoy.
                                                                
Author(s):
 - Wolfgang Foerster, wf@experiment-s.de; wf@inventronik.de
