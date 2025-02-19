Stderr for source:  Path.md_working_3.dat   
Download: [zipped raw stdout](Path.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Path.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GPATH LABEL=pp ARG=t1,t2 REFERENCE=epath.pdb
Maybe a missing space or a typo?
[fv-az1755-505:08503] *** Process received signal ***
[fv-az1755-505:08503] Signal: Aborted (6)
[fv-az1755-505:08503] Signal code:  (-6)
[fv-az1755-505:08503] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc77e445330]
[fv-az1755-505:08503] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc77e49eb2c]
[fv-az1755-505:08503] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc77e44527e]
[fv-az1755-505:08503] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc77e4288ff]
[fv-az1755-505:08503] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc77e8a5ff5]
[fv-az1755-505:08503] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc77e8bb0da]
[fv-az1755-505:08503] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc77e8a5a55]
[fv-az1755-505:08503] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc77e8a5a6f]
[fv-az1755-505:08503] [ 8] plumed(+0x13209)[0x558105603209]
[fv-az1755-505:08503] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc77e42a1ca]
[fv-az1755-505:08503] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc77e42a28b]
[fv-az1755-505:08503] [11] plumed(+0x134a5)[0x5581056034a5]
[fv-az1755-505:08503] *** End of error message ***
</pre>
{% endraw %}
