Stderr for source:  averaging.md_working_4.dat   
Download: [zipped raw stdout](averaging.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](averaging.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/PlumedMain.cpp:903) void PLMD::PlumedMain::readInputWords(const std::vector<std::__cxx11::basic_string<char> >&)
ERROR
I cannot understand line: ACCUMULATE LABEL=a1_denom ARG=a1_weight STRIDE=1 CLEAR=100
Maybe a missing space or a typo?
[fv-az1755-505:07489] *** Process received signal ***
[fv-az1755-505:07489] Signal: Aborted (6)
[fv-az1755-505:07489] Signal code:  (-6)
[fv-az1755-505:07489] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f28ef245330]
[fv-az1755-505:07489] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f28ef29eb2c]
[fv-az1755-505:07489] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f28ef24527e]
[fv-az1755-505:07489] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f28ef2288ff]
[fv-az1755-505:07489] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f28ef6a5ff5]
[fv-az1755-505:07489] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f28ef6bb0da]
[fv-az1755-505:07489] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f28ef6a5a55]
[fv-az1755-505:07489] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f28ef6a5a6f]
[fv-az1755-505:07489] [ 8] plumed(+0x13209)[0x55eb80211209]
[fv-az1755-505:07489] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f28ef22a1ca]
[fv-az1755-505:07489] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f28ef22a28b]
[fv-az1755-505:07489] [11] plumed(+0x134a5)[0x55eb802114a5]
[fv-az1755-505:07489] *** End of error message ***
</pre>
{% endraw %}
