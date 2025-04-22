Stderr for source:  work/plumed_ex5.dat   
Download: [zipped raw stdout](plumed_ex5.dat.plumed_master.stdout.txt.zip) - [zipped raw stderr](plumed_ex5.dat.plumed_master.stderr.txt.zip) 
{% raw %}
<pre>
#! Only the first 1000 rows of the error file are shown below
#! To inspect the full error file, please download the zipped raw stderr file above
WARNING: IFile closed in the middle of reading. seems strange!
terminate called after throwing an instance of 'PLMD::Plumed::ExceptionError'
what():
(core/Action.cpp:375) void PLMD::Action::error(const std::string&) const
ERROR in input to action DUMPGRID with label @12 : keyword ARG is compulsory for this action
[fv-az1279-640:06939] *** Process received signal ***
[fv-az1279-640:06939] Signal: Aborted (6)
[fv-az1279-640:06939] Signal code:  (-6)
[fv-az1279-640:06939] [ 0] /lib/x86_64-linux-gnu/libc.so.6(+0x45330)[0x7f9777e45330]
[fv-az1279-640:06939] [ 1] /lib/x86_64-linux-gnu/libc.so.6(pthread_kill+0x11c)[0x7f9777e9eb2c]
[fv-az1279-640:06939] [ 2] /lib/x86_64-linux-gnu/libc.so.6(gsignal+0x1e)[0x7f9777e4527e]
[fv-az1279-640:06939] [ 3] /lib/x86_64-linux-gnu/libc.so.6(abort+0xdf)[0x7f9777e288ff]
[fv-az1279-640:06939] [ 4] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5ff5)[0x7f97782a5ff5]
[fv-az1279-640:06939] [ 5] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xbb0da)[0x7f97782bb0da]
[fv-az1279-640:06939] [ 6] /lib/x86_64-linux-gnu/libstdc++.so.6(_ZSt10unexpectedv+0x0)[0x7f97782a5a55]
[fv-az1279-640:06939] [ 7] /lib/x86_64-linux-gnu/libstdc++.so.6(+0xa5a6f)[0x7f97782a5a6f]
[fv-az1279-640:06939] [ 8] plumed_master(+0x146dd)[0x5584eb30e6dd]
[fv-az1279-640:06939] [ 9] /lib/x86_64-linux-gnu/libc.so.6(+0x2a1ca)[0x7f9777e2a1ca]
[fv-az1279-640:06939] [10] /lib/x86_64-linux-gnu/libc.so.6(__libc_start_main+0x8b)[0x7f9777e2a28b]
[fv-az1279-640:06939] [11] plumed_master(+0x15365)[0x5584eb30f365]
[fv-az1279-640:06939] *** End of error message ***
</pre>
{% endraw %}
