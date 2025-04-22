Stderr for source:  INSTRUCTIONS.md_working_2.dat   
Download: [zipped raw stdout](INSTRUCTIONS.md_working_2.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](INSTRUCTIONS.md_working_2.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action ENVIRONMENTSIMILARITY with label @s9 : keyword SIGMA could not be read correctly
[fv-az2211-783:06064] *** Process received signal ***
[fv-az2211-783:06064] Signal: Aborted (6)
[fv-az2211-783:06064] Signal code:  (-6)
[fv-az2211-783:06064] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f7bc5045330]
[fv-az2211-783:06064] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f7bc509eb2c]
[fv-az2211-783:06064] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f7bc504527e]
[fv-az2211-783:06064] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f7bc50288ff]
[fv-az2211-783:06064] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f7bc54a5ff5]
[fv-az2211-783:06064] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f7bc54bb0da]
[fv-az2211-783:06064] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f7bc54a5a55]
[fv-az2211-783:06064] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f7bc54a5a6f]
[fv-az2211-783:06064] [ 8] plumed_master(+0x146dd)[0x55aaf94936dd]
[fv-az2211-783:06064] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f7bc502a1ca]
[fv-az2211-783:06064] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f7bc502a28b]
[fv-az2211-783:06064] [11] plumed_master(+0x15365)[0x55aaf9494365]
[fv-az2211-783:06064] *** End of error message ***
</pre>
{% endraw %}
