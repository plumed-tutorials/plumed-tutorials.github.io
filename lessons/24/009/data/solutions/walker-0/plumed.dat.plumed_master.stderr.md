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
[fv-az2211-783:05753] *** Process received signal ***
[fv-az2211-783:05753] Signal: Aborted (6)
[fv-az2211-783:05753] Signal code:  (-6)
[fv-az2211-783:05753] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f43ca645330]
[fv-az2211-783:05753] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f43ca69eb2c]
[fv-az2211-783:05753] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f43ca64527e]
[fv-az2211-783:05753] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f43ca6288ff]
[fv-az2211-783:05753] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f43caaa5ff5]
[fv-az2211-783:05753] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f43caabb0da]
[fv-az2211-783:05753] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f43caaa5a55]
[fv-az2211-783:05753] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f43caaa5a6f]
[fv-az2211-783:05753] [ 8] plumed_master(+0x146dd)[0x5651047516dd]
[fv-az2211-783:05753] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f43ca62a1ca]
[fv-az2211-783:05753] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f43ca62a28b]
[fv-az2211-783:05753] [11] plumed_master(+0x15365)[0x565104752365]
[fv-az2211-783:05753] *** End of error message ***
</pre>
{% endraw %}
