Stderr for source:  Tasks.md_working_4.dat   
Download: [zipped raw stdout](Tasks.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Tasks.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ONES LABEL=ones SIZE=100
Maybe a missing space or a typo?
[fv-az1755-505:06063] *** Process received signal ***
[fv-az1755-505:06063] Signal: Aborted (6)
[fv-az1755-505:06063] Signal code:  (-6)
[fv-az1755-505:06063] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f3272e45330]
[fv-az1755-505:06063] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f3272e9eb2c]
[fv-az1755-505:06063] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f3272e4527e]
[fv-az1755-505:06063] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f3272e288ff]
[fv-az1755-505:06063] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f32732a5ff5]
[fv-az1755-505:06063] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f32732bb0da]
[fv-az1755-505:06063] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f32732a5a55]
[fv-az1755-505:06063] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f32732a5a6f]
[fv-az1755-505:06063] [ 8] plumed(+0x13209)[0x55ef43a55209]
[fv-az1755-505:06063] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f3272e2a1ca]
[fv-az1755-505:06063] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f3272e2a28b]
[fv-az1755-505:06063] [11] plumed(+0x134a5)[0x55ef43a554a5]
[fv-az1755-505:06063] *** End of error message ***
</pre>
{% endraw %}
