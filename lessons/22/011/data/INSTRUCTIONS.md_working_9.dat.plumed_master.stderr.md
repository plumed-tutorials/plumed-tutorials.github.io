Stderr for source:  INSTRUCTIONS.md_working_9.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_9.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_9.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action READ with label dist : could not find file named colvar_reweight.data
[fv-az1690-151:06985] *** Process received signal ***
[fv-az1690-151:06985] Signal: Aborted (6)
[fv-az1690-151:06985] Signal code:  (-6)
[fv-az1690-151:06985] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7fd485045330]
[fv-az1690-151:06985] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7fd48509eb2c]
[fv-az1690-151:06985] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7fd48504527e]
[fv-az1690-151:06985] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7fd4850288ff]
[fv-az1690-151:06985] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7fd4854a5ff5]
[fv-az1690-151:06985] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7fd4854bb0da]
[fv-az1690-151:06985] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7fd4854a5a55]
[fv-az1690-151:06985] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7fd4854a5a6f]
[fv-az1690-151:06985] [ 8] plumed_master(+0x146dd)[0x561e6e6916dd]
[fv-az1690-151:06985] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7fd48502a1ca]
[fv-az1690-151:06985] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7fd48502a28b]
[fv-az1690-151:06985] [11] plumed_master(+0x15365)[0x561e6e692365]
[fv-az1690-151:06985] *** End of error message ***
</pre>
{% endraw %}
