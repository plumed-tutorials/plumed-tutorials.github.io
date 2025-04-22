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
[fv-az2211-783:06863] *** Process received signal ***
[fv-az2211-783:06863] Signal: Aborted (6)
[fv-az2211-783:06863] Signal code:  (-6)
[fv-az2211-783:06863] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f01cbe45330]
[fv-az2211-783:06863] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f01cbe9eb2c]
[fv-az2211-783:06863] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f01cbe4527e]
[fv-az2211-783:06863] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f01cbe288ff]
[fv-az2211-783:06863] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f01cc2a5ff5]
[fv-az2211-783:06863] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f01cc2bb0da]
[fv-az2211-783:06863] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f01cc2a5a55]
[fv-az2211-783:06863] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f01cc2a5a6f]
[fv-az2211-783:06863] [ 8] plumed_master(+0x146dd)[0x5607599296dd]
[fv-az2211-783:06863] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f01cbe2a1ca]
[fv-az2211-783:06863] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f01cbe2a28b]
[fv-az2211-783:06863] [11] plumed_master(+0x15365)[0x56075992a365]
[fv-az2211-783:06863] *** End of error message ***
</pre>
{% endraw %}
