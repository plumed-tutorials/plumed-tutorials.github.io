Stderr for source:  averaging.md_working_10.dat   
Download: [zipped raw stdout](averaging.md_working_10.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_10.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: GATHER_REPLICAS LABEL=d1g ARG=d1
Maybe a missing space or a typo?
[fv-az1755-505:07670] *** Process received signal ***
[fv-az1755-505:07670] Signal: Aborted (6)
[fv-az1755-505:07670] Signal code:  (-6)
[fv-az1755-505:07670] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f6141e45330]
[fv-az1755-505:07670] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f6141e9eb2c]
[fv-az1755-505:07670] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f6141e4527e]
[fv-az1755-505:07670] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f6141e288ff]
[fv-az1755-505:07670] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f61422a5ff5]
[fv-az1755-505:07670] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f61422bb0da]
[fv-az1755-505:07670] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f61422a5a55]
[fv-az1755-505:07670] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f61422a5a6f]
[fv-az1755-505:07670] [ 8] plumed(+0x13209)[0x561c6138d209]
[fv-az1755-505:07670] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f6141e2a1ca]
[fv-az1755-505:07670] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f6141e2a28b]
[fv-az1755-505:07670] [11] plumed(+0x134a5)[0x561c6138d4a5]
[fv-az1755-505:07670] *** End of error message ***
</pre>
{% endraw %}
