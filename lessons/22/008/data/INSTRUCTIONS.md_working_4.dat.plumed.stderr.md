Stderr for source:  INSTRUCTIONS.md_working_4.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: CMUMD LABEL=left GROUP=lj NSV=1 FIXED=0.4 DCR=0.25 CRSIZE=0.1 WF=0.0001 ASYMM=-1 NINT=0.1 NZ=291
Maybe a missing space or a typo?
[fv-az1690-151:07304] *** Process received signal ***
[fv-az1690-151:07304] Signal: Aborted (6)
[fv-az1690-151:07304] Signal code:  (-6)
[fv-az1690-151:07304] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f286de45330]
[fv-az1690-151:07304] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f286de9eb2c]
[fv-az1690-151:07304] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f286de4527e]
[fv-az1690-151:07304] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f286de288ff]
[fv-az1690-151:07304] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f286e2a5ff5]
[fv-az1690-151:07304] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f286e2bb0da]
[fv-az1690-151:07304] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f286e2a5a55]
[fv-az1690-151:07304] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f286e2a5a6f]
[fv-az1690-151:07304] [ 8] plumed(+0x13209)[0x55f257d19209]
[fv-az1690-151:07304] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f286de2a1ca]
[fv-az1690-151:07304] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f286de2a28b]
[fv-az1690-151:07304] [11] plumed(+0x134a5)[0x55f257d194a5]
[fv-az1690-151:07304] *** End of error message ***
</pre>
{% endraw %}
