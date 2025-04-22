Stderr for source:  MDInterfaceII.md_working_1.dat   
Download: [zipped raw stdout](MDInterfaceII.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MDInterfaceII.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: DOMAIN_DECOMPOSITION LABEL=gromacs NATOMS=2000 VALUE1=myposx UNIT1=length PERIODIC1=NO CONSTANT1=False ROLE1=x VALUE2=myposy UNIT2=length PERIODIC2=NO CONSTANT2=False ROLE2=y VALUE3=myposz UNIT3=length PERIODIC3=NO CONSTANT3=False ROLE3=z VALUE4=myMasses UNIT4=mass PERIODIC4=NO CONSTANT4=True ROLE4=m VALUE5=myCharges UNIT5=charge PERIODIC5=NO CONSTANT5=True ROLE5=q PBCLABEL=mybox
Maybe a missing space or a typo?
[fv-az1315-757:05315] *** Process received signal ***
[fv-az1315-757:05315] Signal: Aborted (6)
[fv-az1315-757:05315] Signal code:  (-6)
[fv-az1315-757:05315] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd1b5a45330]
[fv-az1315-757:05315] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd1b5a9eb2c]
[fv-az1315-757:05315] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd1b5a4527e]
[fv-az1315-757:05315] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd1b5a288ff]
[fv-az1315-757:05315] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd1b5ea5ff5]
[fv-az1315-757:05315] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd1b5ebb0da]
[fv-az1315-757:05315] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd1b5ea5a55]
[fv-az1315-757:05315] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd1b5ea5a6f]
[fv-az1315-757:05315] [ 8] plumed(+0x13209)[0x5622b587c209]
[fv-az1315-757:05315] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd1b5a2a1ca]
[fv-az1315-757:05315] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd1b5a2a28b]
[fv-az1315-757:05315] [11] plumed(+0x134a5)[0x5622b587c4a5]
[fv-az1315-757:05315] *** End of error message ***
</pre>
{% endraw %}
