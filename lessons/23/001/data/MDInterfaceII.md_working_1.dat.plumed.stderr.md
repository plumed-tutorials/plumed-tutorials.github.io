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
[fv-az1755-505:05257] *** Process received signal ***
[fv-az1755-505:05257] Signal: Aborted (6)
[fv-az1755-505:05257] Signal code:  (-6)
[fv-az1755-505:05257] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f193b645330]
[fv-az1755-505:05257] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f193b69eb2c]
[fv-az1755-505:05257] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f193b64527e]
[fv-az1755-505:05257] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f193b6288ff]
[fv-az1755-505:05257] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f193baa5ff5]
[fv-az1755-505:05257] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f193babb0da]
[fv-az1755-505:05257] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f193baa5a55]
[fv-az1755-505:05257] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f193baa5a6f]
[fv-az1755-505:05257] [ 8] plumed(+0x13209)[0x55c04e6c4209]
[fv-az1755-505:05257] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f193b62a1ca]
[fv-az1755-505:05257] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f193b62a28b]
[fv-az1755-505:05257] [11] plumed(+0x134a5)[0x55c04e6c44a5]
[fv-az1755-505:05257] *** End of error message ***
</pre>
{% endraw %}
