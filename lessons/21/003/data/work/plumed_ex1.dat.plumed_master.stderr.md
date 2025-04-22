Stderr for source:  work/plumed_ex1.dat   
Download: [zipped raw stdout](plumed_ex1.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex1.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @35 : keyword ARG is compulsory for this action
[fv-az1279-640:06689] *** Process received signal ***
[fv-az1279-640:06689] Signal: Aborted (6)
[fv-az1279-640:06689] Signal code:  (-6)
[fv-az1279-640:06689] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f4614845330]
[fv-az1279-640:06689] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f461489eb2c]
[fv-az1279-640:06689] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f461484527e]
[fv-az1279-640:06689] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f46148288ff]
[fv-az1279-640:06689] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f4614ca5ff5]
[fv-az1279-640:06689] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f4614cbb0da]
[fv-az1279-640:06689] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f4614ca5a55]
[fv-az1279-640:06689] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f4614ca5a6f]
[fv-az1279-640:06689] [ 8] plumed_master(+0x146dd)[0x5561d7ec26dd]
[fv-az1279-640:06689] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f461482a1ca]
[fv-az1279-640:06689] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f461482a28b]
[fv-az1279-640:06689] [11] plumed_master(+0x15365)[0x5561d7ec3365]
[fv-az1279-640:06689] *** End of error message ***
</pre>
{% endraw %}
