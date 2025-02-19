Stderr for source:  Sprint.md_working_2.dat   
Download: [zipped raw stdout](Sprint.md_working_2.dat.plumed.stdout.txt.zip) - [zipped raw stderr](Sprint.md_working_2.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action CONTACT_MATRIX with label s1_mat : No atoms have been read in
[fv-az1755-505:06128] *** Process received signal ***
[fv-az1755-505:06128] Signal: Aborted (6)
[fv-az1755-505:06128] Signal code:  (-6)
[fv-az1755-505:06128] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fcd31245330]
[fv-az1755-505:06128] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fcd3129eb2c]
[fv-az1755-505:06128] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fcd3124527e]
[fv-az1755-505:06128] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fcd312288ff]
[fv-az1755-505:06128] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fcd316a5ff5]
[fv-az1755-505:06128] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fcd316bb0da]
[fv-az1755-505:06128] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fcd316a5a55]
[fv-az1755-505:06128] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fcd316a5a6f]
[fv-az1755-505:06128] [ 8] plumed(+0x13209)[0x55d820b4b209]
[fv-az1755-505:06128] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fcd3122a1ca]
[fv-az1755-505:06128] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fcd3122a28b]
[fv-az1755-505:06128] [11] plumed(+0x134a5)[0x55d820b4b4a5]
[fv-az1755-505:06128] *** End of error message ***
</pre>
{% endraw %}
