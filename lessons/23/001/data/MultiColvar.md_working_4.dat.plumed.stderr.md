Stderr for source:  MultiColvar.md_working_4.dat   
Download: [zipped raw stdout](MultiColvar.md_working_4.dat.plumed.stdout.txt.zip) - [zipped raw stderr](MultiColvar.md_working_4.dat.plumed.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:273) void PLMD::Action::error(const std::string&) const
ERROR in input to action DISTANCE with label d1 : Number of specified atoms should be 2
[fv-az1755-505:05484] *** Process received signal ***
[fv-az1755-505:05484] Signal: Aborted (6)
[fv-az1755-505:05484] Signal code:  (-6)
[fv-az1755-505:05484] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f2680845330]
[fv-az1755-505:05484] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f268089eb2c]
[fv-az1755-505:05484] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f268084527e]
[fv-az1755-505:05484] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f26808288ff]
[fv-az1755-505:05484] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f2680ca5ff5]
[fv-az1755-505:05484] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f2680cbb0da]
[fv-az1755-505:05484] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f2680ca5a55]
[fv-az1755-505:05484] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f2680ca5a6f]
[fv-az1755-505:05484] [ 8] plumed(+0x13209)[0x561dc93b8209]
[fv-az1755-505:05484] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f268082a1ca]
[fv-az1755-505:05484] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f268082a28b]
[fv-az1755-505:05484] [11] plumed(+0x134a5)[0x561dc93b84a5]
[fv-az1755-505:05484] *** End of error message ***
</pre>
{% endraw %}
