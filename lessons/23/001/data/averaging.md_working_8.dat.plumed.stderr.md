Stderr for source:  averaging.md_working_8.dat   
Download: [zipped raw stdout](averaging.md_working_8.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_8.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: MEAN LABEL=c1_mean ARG=c1 PERIODIC=NO
Maybe a missing space or a typo?
[fv-az1755-505:07590] *** Process received signal ***
[fv-az1755-505:07590] Signal: Aborted (6)
[fv-az1755-505:07590] Signal code:  (-6)
[fv-az1755-505:07590] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fdaa9645330]
[fv-az1755-505:07590] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fdaa969eb2c]
[fv-az1755-505:07590] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fdaa964527e]
[fv-az1755-505:07590] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fdaa96288ff]
[fv-az1755-505:07590] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fdaa9aa5ff5]
[fv-az1755-505:07590] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fdaa9abb0da]
[fv-az1755-505:07590] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fdaa9aa5a55]
[fv-az1755-505:07590] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fdaa9aa5a6f]
[fv-az1755-505:07590] [ 8] plumed(+0x13209)[0x55fa8da52209]
[fv-az1755-505:07590] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fdaa962a1ca]
[fv-az1755-505:07590] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fdaa962a28b]
[fv-az1755-505:07590] [11] plumed(+0x134a5)[0x55fa8da524a5]
[fv-az1755-505:07590] *** End of error message ***
</pre>
{% endraw %}
