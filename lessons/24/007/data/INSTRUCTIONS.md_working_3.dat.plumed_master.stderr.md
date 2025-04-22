Stderr for source:  INSTRUCTIONS.md_working_3.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_3.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_3.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action METAD with label m : Calculating the transition bias on the fly works only with a grid
[fv-az2211-783:06027] *** Process received signal ***
[fv-az2211-783:06027] Signal: Aborted (6)
[fv-az2211-783:06027] Signal code:  (-6)
[fv-az2211-783:06027] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7ff98ce45330]
[fv-az2211-783:06027] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7ff98ce9eb2c]
[fv-az2211-783:06027] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7ff98ce4527e]
[fv-az2211-783:06027] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7ff98ce288ff]
[fv-az2211-783:06027] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7ff98d2a5ff5]
[fv-az2211-783:06027] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7ff98d2bb0da]
[fv-az2211-783:06027] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7ff98d2a5a55]
[fv-az2211-783:06027] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7ff98d2a5a6f]
[fv-az2211-783:06027] [ 8] plumed_master(+0x146dd)[0x5582267566dd]
[fv-az2211-783:06027] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7ff98ce2a1ca]
[fv-az2211-783:06027] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7ff98ce2a28b]
[fv-az2211-783:06027] [11] plumed_master(+0x15365)[0x558226757365]
[fv-az2211-783:06027] *** End of error message ***
</pre>
{% endraw %}
