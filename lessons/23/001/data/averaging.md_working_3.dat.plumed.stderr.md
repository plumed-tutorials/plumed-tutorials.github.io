Stderr for source:  averaging.md_working_3.dat   
Download: [zipped raw stdout](averaging.md_working_3.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_3.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ACCUMULATE LABEL=a1_denom ARG=a1_weight STRIDE=1
Maybe a missing space or a typo?
[fv-az1755-505:07457] *** Process received signal ***
[fv-az1755-505:07457] Signal: Aborted (6)
[fv-az1755-505:07457] Signal code:  (-6)
[fv-az1755-505:07457] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7faf8e245330]
[fv-az1755-505:07457] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7faf8e29eb2c]
[fv-az1755-505:07457] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7faf8e24527e]
[fv-az1755-505:07457] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7faf8e2288ff]
[fv-az1755-505:07457] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7faf8e6a5ff5]
[fv-az1755-505:07457] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7faf8e6bb0da]
[fv-az1755-505:07457] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7faf8e6a5a55]
[fv-az1755-505:07457] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7faf8e6a5a6f]
[fv-az1755-505:07457] [ 8] plumed(+0x13209)[0x5578f9fc2209]
[fv-az1755-505:07457] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7faf8e22a1ca]
[fv-az1755-505:07457] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7faf8e22a28b]
[fv-az1755-505:07457] [11] plumed(+0x134a5)[0x5578f9fc24a5]
[fv-az1755-505:07457] *** End of error message ***
</pre>
{% endraw %}
