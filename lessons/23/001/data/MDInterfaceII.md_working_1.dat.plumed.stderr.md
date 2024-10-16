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
[fv-az1426-552:04134] *** Process received signal ***
[fv-az1426-552:04134] Signal: Aborted (6)
[fv-az1426-552:04134] Signal code:  (-6)
[fv-az1426-552:04134] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x42520)[0x7f1a9d642520]
[fv-az1426-552:04134] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x12c)[0x7f1a9d6969fc]
[fv-az1426-552:04134] [ 2] /lib/x86_64-linux-gnu/libc.so.6(raise+0x16)[0x7f1a9d642476]
[fv-az1426-552:04134] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xd3)[0x7f1a9d6287f3]
[fv-az1426-552:04134] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa2b9e)[0x7f1a9daa2b9e]
[fv-az1426-552:04134] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae20c)[0x7f1a9daae20c]
[fv-az1426-552:04134] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xae277)[0x7f1a9daae277]
[fv-az1426-552:04134] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(__cxa_rethrow+0x4b)[0x7f1a9daae52b]
[fv-az1426-552:04134] [ 8] plumed(+0x12f48)[0x56117e729f48]
[fv-az1426-552:04134] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x29d90)[0x7f1a9d629d90]
[fv-az1426-552:04134] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x80)[0x7f1a9d629e40]
[fv-az1426-552:04134] [11] plumed(+0x131e5)[0x56117e72a1e5]
[fv-az1426-552:04134] *** End of error message ***
</pre>
{% endraw %}
