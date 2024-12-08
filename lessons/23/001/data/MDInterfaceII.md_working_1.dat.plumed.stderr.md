Stderr for source:  MDInterfaceII.md_working_1.dat   
Download: [zipped raw stdout](MDInterfaceII.md_working_1.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MDInterfaceII.md_working_1.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:824) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: DOMAIN_DECOMPOSITION LABEL=gromacs NATOMS=2000 VALUE1=myposx UNIT1=length PERIODIC1=NO CONSTANT1=False ROLE1=x VALUE2=myposy UNIT2=length PERIODIC2=NO CONSTANT2=False ROLE2=y VALUE3=myposz UNIT3=length PERIODIC3=NO CONSTANT3=False ROLE3=z VALUE4=myMasses UNIT4=mass PERIODIC4=NO CONSTANT4=True ROLE4=m VALUE5=myCharges UNIT5=charge PERIODIC5=NO CONSTANT5=True ROLE5=q PBCLABEL=mybox
Maybe a missing space or a typo?
[fv-az1020-777:03968] *** Process received signal ***
[fv-az1020-777:03968] Signal: Aborted (6)
[fv-az1020-777:03968] Signal code:  (-6)
[fv-az1020-777:03968] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f5083e42520]
[fv-az1020-777:03968] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f5083e969fc]
[fv-az1020-777:03968] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f5083e42476]
[fv-az1020-777:03968] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f5083e287f3]
[fv-az1020-777:03968] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f50842a2b9e]
[fv-az1020-777:03968] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f50842ae20c]
[fv-az1020-777:03968] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f50842ae277]
[fv-az1020-777:03968] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f50842ae52b]
[fv-az1020-777:03968] [ 8] plumed(+0x12f48)[0x556aafb14f48]
[fv-az1020-777:03968] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f5083e29d90]
[fv-az1020-777:03968] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f5083e29e40]
[fv-az1020-777:03968] [11] plumed(+0x131e5)[0x556aafb151e5]
[fv-az1020-777:03968] *** End of error message ***
</pre>
{% endraw %}
