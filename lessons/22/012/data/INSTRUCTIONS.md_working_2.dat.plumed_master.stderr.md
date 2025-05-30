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
[pkrvmf6wy0o8zjz:59643] *** Process received signal ***
[pkrvmf6wy0o8zjz:59643] Signal: Aborted (6)
[pkrvmf6wy0o8zjz:59643] Signal code:  (-6)
[pkrvmf6wy0o8zjz:59643] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9e38245330]
[pkrvmf6wy0o8zjz:59643] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9e3829eb2c]
[pkrvmf6wy0o8zjz:59643] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9e3824527e]
[pkrvmf6wy0o8zjz:59643] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9e382288ff]
[pkrvmf6wy0o8zjz:59643] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f9e386a5ff5]
[pkrvmf6wy0o8zjz:59643] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f9e386bb0da]
[pkrvmf6wy0o8zjz:59643] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f9e386a5a55]
[pkrvmf6wy0o8zjz:59643] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f9e386a5a6f]
[pkrvmf6wy0o8zjz:59643] [ 8] plumed_master(+0x146dd)[0x55e48700a6dd]
[pkrvmf6wy0o8zjz:59643] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9e3822a1ca]
[pkrvmf6wy0o8zjz:59643] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9e3822a28b]
[pkrvmf6wy0o8zjz:59643] [11] plumed_master(+0x15365)[0x55e48700b365]
[pkrvmf6wy0o8zjz:59643] *** End of error message ***
</pre>
{% endraw %}
