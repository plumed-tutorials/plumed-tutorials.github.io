Stderr for source:  ./solutions/walker-0/plumed.dat   
Download: [zipped raw stdout](plumed.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action HBOND_MATRIX with label hbmat1 : cannot understand the following words from the input line : SUM
[fv-az1755-505:05377] *** Process received signal ***
[fv-az1755-505:05377] Signal: Aborted (6)
[fv-az1755-505:05377] Signal code:  (-6)
[fv-az1755-505:05377] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fc243e45330]
[fv-az1755-505:05377] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fc243e9eb2c]
[fv-az1755-505:05377] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fc243e4527e]
[fv-az1755-505:05377] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fc243e288ff]
[fv-az1755-505:05377] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fc2442a5ff5]
[fv-az1755-505:05377] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fc2442bb0da]
[fv-az1755-505:05377] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fc2442a5a55]
[fv-az1755-505:05377] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fc2442a5a6f]
[fv-az1755-505:05377] [ 8] plumed_master(+0x146dd)[0x55fac10706dd]
[fv-az1755-505:05377] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fc243e2a1ca]
[fv-az1755-505:05377] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fc243e2a28b]
[fv-az1755-505:05377] [11] plumed_master(+0x15365)[0x55fac1071365]
[fv-az1755-505:05377] *** End of error message ***
</pre>
{% endraw %}
