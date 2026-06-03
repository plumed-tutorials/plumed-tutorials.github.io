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
[runnervm3jyl0:46929] *** Process received signal ***
[runnervm3jyl0:46929] Signal: Aborted (6)
[runnervm3jyl0:46929] Signal code:  (-6)
[runnervm3jyl0:46929] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f83bfc45330]
[runnervm3jyl0:46929] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f83bfc9eb2c]
[runnervm3jyl0:46929] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f83bfc4527e]
[runnervm3jyl0:46929] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f83bfc288ff]
[runnervm3jyl0:46929] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f83c00a5ff5]
[runnervm3jyl0:46929] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f83c00bb0da]
[runnervm3jyl0:46929] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f83c00a5a55]
[runnervm3jyl0:46929] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f83c00a5a6f]
[runnervm3jyl0:46929] [ 8] plumed(+0x13209)[0x564b2faa1209]
[runnervm3jyl0:46929] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f83bfc2a1ca]
[runnervm3jyl0:46929] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f83bfc2a28b]
[runnervm3jyl0:46929] [11] plumed(+0x134a5)[0x564b2faa14a5]
[runnervm3jyl0:46929] *** End of error message ***
</pre>
{% endraw %}
