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
[pkrvmbietmlfzoi:34579] *** Process received signal ***
[pkrvmbietmlfzoi:34579] Signal: Aborted (6)
[pkrvmbietmlfzoi:34579] Signal code:  (-6)
[pkrvmbietmlfzoi:34579] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fa5d3245330]
[pkrvmbietmlfzoi:34579] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fa5d329eb2c]
[pkrvmbietmlfzoi:34579] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fa5d324527e]
[pkrvmbietmlfzoi:34579] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fa5d32288ff]
[pkrvmbietmlfzoi:34579] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fa5d36a5ff5]
[pkrvmbietmlfzoi:34579] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fa5d36bb0da]
[pkrvmbietmlfzoi:34579] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fa5d36a5a55]
[pkrvmbietmlfzoi:34579] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fa5d36a5a6f]
[pkrvmbietmlfzoi:34579] [ 8] plumed(+0x13209)[0x556d190f8209]
[pkrvmbietmlfzoi:34579] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fa5d322a1ca]
[pkrvmbietmlfzoi:34579] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fa5d322a28b]
[pkrvmbietmlfzoi:34579] [11] plumed(+0x134a5)[0x556d190f84a5]
[pkrvmbietmlfzoi:34579] *** End of error message ***
</pre>
{% endraw %}
