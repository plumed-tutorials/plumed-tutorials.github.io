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
[pkrvmf6wy0o8zjz:58686] *** Process received signal ***
[pkrvmf6wy0o8zjz:58686] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:58686] Signal code:  (-6)
[pkrvmf6wy0o8zjz:58686] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9817245330]
[pkrvmf6wy0o8zjz:58686] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f981729eb2c]
[pkrvmf6wy0o8zjz:58686] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f981724527e]
[pkrvmf6wy0o8zjz:58686] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f98172288ff]
[pkrvmf6wy0o8zjz:58686] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f98176a5ff5]
[pkrvmf6wy0o8zjz:58686] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f98176bb0da]
[pkrvmf6wy0o8zjz:58686] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f98176a5a55]
[pkrvmf6wy0o8zjz:58686] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f98176a5a6f]
[pkrvmf6wy0o8zjz:58686] [ 8] plumed(+0x13209)[0x55e99af9e209]
[pkrvmf6wy0o8zjz:58686] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f981722a1ca]
[pkrvmf6wy0o8zjz:58686] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f981722a28b]
[pkrvmf6wy0o8zjz:58686] [11] plumed(+0x134a5)[0x55e99af9e4a5]
[pkrvmf6wy0o8zjz:58686] *** End of error message ***
</pre>
{% endraw %}
