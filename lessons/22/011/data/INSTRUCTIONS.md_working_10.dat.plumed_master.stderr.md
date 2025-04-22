Stderr for source:  INSTRUCTIONS.md_working_10.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_10.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_10.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[fv-az2211-783:06912] *** Process received signal ***
[fv-az2211-783:06912] Signal: Aborted (6)
[fv-az2211-783:06912] Signal code:  (-6)
[fv-az2211-783:06912] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fedef045330]
[fv-az2211-783:06912] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fedef09eb2c]
[fv-az2211-783:06912] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fedef04527e]
[fv-az2211-783:06912] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fedef0288ff]
[fv-az2211-783:06912] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fedef4a5ff5]
[fv-az2211-783:06912] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fedef4bb0da]
[fv-az2211-783:06912] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fedef4a5a55]
[fv-az2211-783:06912] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fedef4a5a6f]
[fv-az2211-783:06912] [ 8] plumed_master(+0x146dd)[0x55e4edee16dd]
[fv-az2211-783:06912] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fedef02a1ca]
[fv-az2211-783:06912] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fedef02a28b]
[fv-az2211-783:06912] [11] plumed_master(+0x15365)[0x55e4edee2365]
[fv-az2211-783:06912] *** End of error message ***
</pre>
{% endraw %}
